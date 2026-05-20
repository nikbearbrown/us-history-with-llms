# Running Project Candidates — US History with LLMs

*Saved 2026-05-10. Four candidates. Pick one before Chapter 1 enrichment begins; the choice shapes every LLM Exercise in the book.*

*Each candidate is a single artifact the student builds incrementally — one substantial entry per chapter, 32 entries total by the end of the book. Each entry teaches both history and the use of Claude. The deliverable at chapter end is real (something the student can show someone), not preparatory.*

---

## Option 1 — The Verification Logbook

**What it is.** A running document where each chapter contributes one entry: a specific claim the student asked Claude (or ChatGPT, or Gemini) to make about that chapter's material, the primary source the student checked it against, and the verdict — *verified*, *wrong in a specific way*, or *contested between historians*. Entries include the exact prompt, the model's exact response, the source consulted with citation, and a one-paragraph reading of what the student now believes.

**Final deliverable.** A ~150–200-entry document — the student's personal historiography of where LLMs are reliable in US history and where they aren't. By the end the student can predict, before asking, which kinds of questions Claude will handle well and which it will smooth over.

**Why it fits this book.** It is the book's premise made operational. The book argues that LLMs are instruments with known precision and failure modes; this project is the student building their own calibration document over a semester. The Chapter Map already identifies five reliable LLM-error sites (Emancipation Proclamation, Battle of New Orleans timing, Compromise of 1877, Philippine-American War, Social Security exclusions) — these become anchor entries the student is guided to early. The other ~150 are theirs to discover.

**Adaptability.** Two students will produce different logbooks. A pre-med student might focus on disease history (1918 flu, smallpox in the Americas, the Tuskegee experiment). A future historian of technology might focus on infrastructure (canals, railroads, the Internet). A novelist might focus on individual lives. The project's structure is fixed; its content is the student's interests as filtered through the syllabus.

**Tool path.** Claude Project — persistent context across the semester. The system prompt holds the standing instructions for what an entry looks like; each chapter session adds to it. Cowork is the file home if the student wants the logbook to live on their machine. Claude Code is unnecessary unless the student wants to wrap the logbook in a script (search, tagging, analytics).

**Chapter 00 connection.** Chapter 00 introduces the logbook concept and the student creates their first entry — testing Claude on the Battle of New Orleans / Treaty of Ghent timing, comparing to primary sources, writing the verdict. Every subsequent chapter's LLM Exercise adds an entry.

**Strongest pitch.** This is the project that does the most to teach the book's actual claim. By the end the student has *evidence* that LLMs have specific competencies and specific failure patterns, and they can articulate where the line falls. That's transferable to every other domain they'll use LLMs in.

---

## Option 2 — The Counter-Narrative Wiki

**What it is.** A 32-entry wiki where each chapter contributes one "contested point" — a topic where the standard textbook narrative is challenged by working historians, with Claude used to surface the alternative reading and the student responsible for verifying both sides. Each entry has: the orthodox narrative, the contested reading, the historians on each side (named, with works cited), the primary-source evidence that distinguishes them, and the student's current reading with reasoning.

**Final deliverable.** A wiki of 32 contested points across American history — a useful artifact in its own right, and a working knowledge of where the historiography is alive.

**Why it fits this book.** The Voice notes in `book.md` say "Contested interpretations stay contested" and "The Civil War's causes, the New Deal's effects, the Cold War's necessity — these are live disputes among historians." This project operationalizes that commitment. It teaches a habit of looking for the dispute behind the textbook sentence.

**Adaptability.** Different students will pick different fights. One student will dig into the historiography of the New Deal's effectiveness; another will work on the Civil War's causes vs. the "states' rights" framing; another on whether the dropping of the atomic bombs was militarily necessary. The structure is fixed; the contested-point selection is the student's intellectual signature.

**Tool path.** Claude Project (persistent system prompt establishing the entry format) + Cowork for file storage. Optional: Claude Code to build a static site from the markdown files (a real, public-shareable wiki at the end of the semester).

**Chapter 00 connection.** Chapter 00 introduces the practice of asking Claude to surface a contested interpretation, then verifying against the historiography. Worked example in Chapter 00: a contested point from Chapter 8 (was the War of 1812 a "Second War of Independence" or a war of aggression against Canada?).

**Strongest pitch.** This is the project that produces the most intellectually substantive artifact. By the end the student has demonstrated mastery of *what historians fight about and why* — a different and arguably deeper outcome than the verification logbook.

**Risk.** Heavier lift per chapter. Some chapters have less obvious contested points (the early colonial period) and finding one good enough to write up may strain the project's pace.

---

## Option 3 — The Source Triangulation Agent

**What it is.** Across the semester the student builds a single Claude Project — a "historiography assistant" — that takes a US-history claim as input and returns a triangulated analysis: (1) what the orthodox textbook narrative says, (2) what the primary sources show, (3) what current scholarship argues. Each chapter contributes one worked triangulation that gets added to the project's example library, and the system prompt is refined chapter by chapter as the student notices what makes the assistant better.

**Final deliverable.** A working Claude Project with 32 worked examples and a tuned system prompt — a tool the student (and anyone else they share it with) can use after the course to triangulate any historical claim.

**Why it fits this book.** This is the most LLM-native of the four options. The student isn't just learning history; they're building a tool that does what the book argues good historical practice should do, using the instrument the book is teaching them to use. The reflexive commitment is built in — every chapter, the student is testing whether their own tool is doing what they claim it does.

**Adaptability.** The system prompt can be tuned for different audiences (high school, undergrad, public history, journalism). The triangulation examples reflect the student's interests. A version aimed at journalists would emphasize fact-checking; a version aimed at teachers would emphasize lesson-planning.

**Tool path.** Claude Project (this *is* the project). Cowork for storing the example library and version history of the system prompt. Optional: Claude Code for analytics over the triangulation library.

**Chapter 00 connection.** Chapter 00 walks the student through creating the initial Claude Project — empty system prompt, one worked triangulation, the practice of refining the prompt as the student notices patterns.

**Strongest pitch.** This is the project that most directly makes the student a more capable LLM user. The artifact is *itself* an LLM. By the end the student has internalized prompt design through doing it 32 times on a single project.

**Risk.** Most technically demanding. Students with no prior LLM experience may struggle with the abstraction of "tuning a system prompt" early in the semester. Mitigation: Chapter 00 includes a worked example of system-prompt iteration, and the first three chapters' exercises are explicit about what to change.

---

## Option 4 — The Voices Anthology

**What it is.** Across the semester the student curates a primary-source anthology — each chapter contributes 1–3 voices (letters, speeches, songs, interviews, court testimony, newspaper editorials) that complicate or extend the textbook narrative. Claude assists with search, paraphrase-vs-quote decisions, contextualization, and (for older sources) translation or modernization of orthography. The student is responsible for the curatorial argument: why *these* voices, in *this* order, telling *this* story.

**Final deliverable.** An anthology of 50–80 primary-source excerpts with student commentary, organized as a usable reader. By the end the student has done a curator's work on American history.

**Why it fits this book.** The Voice notes in `book.md` are explicit: "Sources are the argument. US history is a field where the question of whose account is part of the substance." This project makes the student do that work for an entire semester. It also forces the student into archives (online ones, mostly — Library of Congress, National Archives, university digital collections), which is itself a skill the book wants to teach.

**Adaptability.** The most flexible of the four. The anthology can be thematic (Black voices, women's voices, immigrant voices, dissenting voices), regional (a single state across 32 chapters), or contrarian (voices the textbook narrative omits). Two students producing very different anthologies is the point.

**Tool path.** Cowork (the anthology is files on disk) + Claude chat for assist tasks. Claude Project is useful for keeping a curatorial system prompt across sessions. Claude Code is optional — if the student wants to build a searchable digital edition at the end.

**Chapter 00 connection.** Chapter 00 introduces the curatorial practice and the role Claude plays (research assistant for finding candidates, *not* author of commentary). The student picks an organizing principle in Chapter 1 and the anthology is built around it.

**Strongest pitch.** This is the project that produces the most beautiful artifact and the most direct training in primary-source literacy. It is also the project that does the most to deflate the "LLMs replace humanists" claim — the LLM is genuinely useful here, and equally clearly not doing the curatorial work.

**Risk.** Heaviest dependence on outside sources. A semester with limited archive access (online or otherwise) constrains the project. Mitigation: every chapter's exercise names 2–3 well-digitized collections relevant to that period (Founders Online, the Frederick Douglass Papers, the FDR Library, etc.).

---

## How to choose

Three questions to ask:

**1. What is the student supposed to be able to do at the end?**
- *Logbook:* know where LLMs are reliable in this domain
- *Wiki:* know what historians fight about
- *Agent:* build LLM tools for historical work
- *Anthology:* read and curate primary sources

**2. What is the artifact the student walks away with?**
- *Logbook:* a calibration document, mostly useful to the student personally
- *Wiki:* a 32-entry reference work, useful to anyone studying US history
- *Agent:* a working Claude Project, shareable as a tool
- *Anthology:* a primary-source reader, possibly publishable

**3. What kind of mind does the project reward?**
- *Logbook:* curious, skeptical, taxonomic
- *Wiki:* argumentative, historiographically-minded
- *Agent:* systems-oriented, builder-type
- *Anthology:* curatorial, literary, archive-loving

---

## My recommendation

**Option 1 — The Verification Logbook** — is the right default for the book's stated purpose. The book is a survey textbook that uses LLMs as instruments; the logbook is the project that most directly trains the instrument-use skill the book promises. The other three are excellent projects, and may be better fits for specific courses or readers, but they answer slightly different questions:

- Option 2 (Wiki) is a better fit for a *historiography* course — the framing is "learn to argue about history."
- Option 3 (Agent) is a better fit for an *applied AI / digital humanities* course — the framing is "build LLM tools."
- Option 4 (Anthology) is a better fit for an *American Studies / sources* course — the framing is "learn to read voices."

The book is, by its outline, none of those. It is the survey with LLMs threaded through. Option 1 fits.

A defensible alternative: build the book around **Option 1 as default** and **offer Option 4 as an instructor swap** in Chapter 00 — instructors who care more about primary-source pedagogy can substitute the anthology without changing the rest of the book's structure. (Options 2 and 3 require deeper rewrites and shouldn't be presented as swap-ins.)

---

*Pick one. The next step is enriching Chapter 1 around the chosen project.*
