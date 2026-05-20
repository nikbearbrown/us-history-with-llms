# Pushback on the "With LLMs" enrichment prompt

*Saved 2026-05-10 before running anything. Read this, decide, then we proceed.*

---

## What I actually found

**Book state: B (source subfolders), with a wrinkle.**

`chapters/` holds 32 numbered subfolders. Each contains 4–6 source `.md` files named with OpenStax module IDs (`m49967`, `m50208`, etc.). I spot-checked `01-the-americas-europe-and-africa-before-1492/01-m49967.md` — it's OpenStax *U.S. History* content, lightly converted to markdown, with CNXML figure tags still present (`<figure id="CNX_History_01_00_ThreeWomen">`).

So this is technically a B/C hybrid: subfolder structure looks like B, but the source is external (OpenStax) and the conversion isn't clean. The prompt's State C mapping step still applies — these `.md` files are partially-converted source, not finished chapters.

Wrinkle: chapter 32 contains an extra `06-m00001.md`. That ID isn't OpenStax. Someone added something. I haven't read it yet.

**`book.md` is mostly unfilled.** Audience: TBD. Scope: TBD. Prerequisites: TBD. Subtitle: TBD. The Voice notes section is the only substantive part.

**`outline.md` is empty.** Both "To write" and "Drafted" sections are empty placeholders.

**`_toc.md` lists source files**, not chapter files. It's pointing at the OpenStax modules.

---

## The real problems with running this prompt now

### 1. The workshop's CLAUDE.md says exercises are embedded in `/chapter`, not added later

§8 of root CLAUDE.md is explicit:

> Exercises are embedded — the workshop does not maintain a separate `/mega` skill.

This enrichment prompt is `/mega` writ large. It creates a parallel workflow: write chapters first, then bolt on Dig Deeper + LLM Exercises in a second pass. The workshop's design is the opposite — the chapter scaffolding itself includes graduated exercises (warm-up → application → synthesis → challenge), built in during drafting because they shape what the chapter teaches.

Two ways out:
- **Fold the prompt into `/chapter`.** "Dig Deeper" and "LLM Exercise" become required components inside the existing 8-section scaffold. One pass, not two.
- **Knowingly run a parallel track** and accept that you're operating outside the workshop's method. Defensible if this is a one-off enrichment for State A books in the series — *not* for States B and C where chapters are still being drafted.

I'd pick the first.

### 2. Writing 32 OpenStax-sourced chapters in batch violates the human review gate

CLAUDE.md §7 hard rule 4:

> The human review gate is inviolable. Every draft lands in `books/[book-slug]/chapters/YYYY-MM-DD-chapter-slug.md`. Nik reviews. Nik approves.

The prompt as written says "process alphabetically." That's batch generation of ~190,000 words of original drafting before you see any of it. By chapter 8 the voice will have drifted; by chapter 20 the cross-references will be wrong; by chapter 32 there will be claims that contradict claims in chapter 5. And you won't have read any of it.

A `/chapter` run produces one chapter, surfaces it for review, logs to `logs/log.csv`, moves the topic on `outline.md`, stops. That's the unit. Batch operation breaks every gate the workshop has.

### 3. `book.md` isn't filled in — every chapter would be miscalibrated

The book has no specified audience, scope, or prerequisites. The voice notes are good but they don't tell a drafter:

- Is this for AP US History students (16-year-olds) or graduate seminar (24-year-olds)? The reading level for "I conclude" versus "the historiography splits" is different.
- Does the book cover 1491–present or 1789–present? OpenStax goes pre-Columbian; some surveys start at the Constitution.
- Does the LLM thread assume the student has used ChatGPT before, or are we teaching the chat interface from scratch?

Drafting 32 chapters against unfilled metadata is committing to choices that should be deliberate. Fix `book.md` first.

### 4. Source rewriting against primary sources is much more work than the prompt acknowledges

CLAUDE.md §7 hard rules 1, 2, 3:

> No fabricated sources... Primary sources where possible... Every contestable factual claim carries a link.

OpenStax is an aggregator, not a primary source. A chapter on "The Americas before 1492" cites archaeological surveys, anthropological work, specific scholars (Jared Diamond, Charles Mann, Alfred Crosby, etc.). The workshop method says the chapter rewrite needs to trace claims back — not just inherit OpenStax's framing.

This isn't impossible, but it changes the time estimate. A `/chapter` run with proper primary-source verification is 30–60 minutes of focused work *per chapter*, not parallelizable.

### 5. The prompt assumes a v1.1 style document that isn't here

> Apply the Attenborough × Feynman v1.1 style and the 8-section chapter structure (specified in the parent workflow document)

There's no "parent workflow document." The workshop's voice ground truth lives in root `style/` and per-book `style/`. Both are referenced in CLAUDE.md §10. I should check whether either is populated before any drafting starts. If both are empty, the first chapter is voice-setting and needs deliberate calibration — not a chapter to delegate to a batch run.

### 6. The "delete source subfolder after verification" step is dangerous

Prompt step B6 says to remove `BOOK_DIR/chapters/NAME/` after verification. Even gated on verification, this destroys the only intact copy of the OpenStax source. If a later chapter needs to cross-reference a removed source — or if the voice calibration changes and chapter 4 needs to be re-drafted from source — that source is gone. Keep the subfolders. Disk is cheap. Moving them to `_source/NAME/` is fine. Deletion is not.

### 7. The "Running Project" idea is genuinely good for this book, and the prompt undersells it

A US-history-with-LLMs Running Project is the place where the book's premise lives or dies. The whole pitch is "Claude as instrument, like a balance." A project where the student maintains, across 32 chapters, *a single artifact that documents what they verified, what Claude got wrong, and where the historiography is contested* — that's the book's argument made concrete. The prompt treats Running Projects as a generic feature; for this book they're the spine.

---

## What I think we should do instead

Phased, with stop-points. Not 32 chapters in a run.

**Phase 1 — Fix the foundation.** Fill out `book.md` (audience, scope, prerequisites). Decide what `style/` contains. Decide whether the OpenStax dependency is acknowledged in `book.md` or hidden. Decide periodization (does the book really need all 32 OpenStax chapters or is this a 12-chapter survey with the others as appendix?). This is a conversation, not a generation.

**Phase 2 — Move source out of `chapters/`.** Rename `chapters/01-…/` to `_source/01-…/` so the workshop's filename convention works (chapter files in `chapters/`, source elsewhere). Don't delete.

**Phase 3 — Chapter 00.** Generate it as the prompt describes, with the LLM-as-instrument framing native to this book. Standalone. Doesn't depend on any survey content. This is a useful first artifact and a good voice calibration exercise. Review, revise, settle voice.

**Phase 4 — Running Project candidates.** Propose 3–5, you pick one. Without this, every chapter exercise is improvised and the project arc won't be visible.

**Phase 5 — Pilot Chapter 1.** Write one full chapter end-to-end, with Dig Deeper + LLM Exercise embedded (folded into `/chapter`, not bolted on). Review. Iterate. Lock the template.

**Phase 6 — Roll forward.** Chapters 2–32 in subsequent sessions, one or two per session, each reviewed. Update `outline.md` and `logs/log.csv` per the workshop protocol. This is months of work, not a single Cowork run.

---

## What I'd like you to decide

Three forks:

**Fork A — Do it the workshop way.** I stop here, you fill in `book.md`, then we generate Chapter 00 next session and pick the Running Project. Slow, correct.

**Fork B — Do the prompt's flow but capped.** I generate Chapter 00 now (no survey content), then the Chapter Map (extracted from OpenStax sources without rewriting them yet), then propose Running Projects. We stop there. No survey-chapter drafting happens in this session. Honors the prompt's order without batch-drafting.

**Fork C — Run the full prompt and accept the costs.** I rewrite all 32 chapters from OpenStax source in this and successive sessions, enrich each, generate Chapter 00 last. You'll get a complete book draft fast. Voice drift, source verification gaps, and review-gate bypass are the price.

I'd pick B. It gets you visible artifacts (Chapter 00 + Chapter Map + Project options) without committing to drafting choices that haven't been calibrated yet.

What do you want?
