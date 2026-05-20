# Revision Notes

Track what you've added, removed, or rewritten here.

---

## 2026-05-10 — "With LLMs" enrichment run, Fork B (Chapter 00 + Chapter Map + Project options only; no survey-chapter drafting)

**Book state detected:** B/C hybrid. `chapters/` contains 32 numbered subfolders (B-shaped), each holding OpenStax source `.md` files with CNXML artifacts (C-shaped — external source, partial conversion).

**Pushback first.** Issues with the prompt as written and with applying it to this book in its current state were saved to `_notes-enrichment-pushback.md`. Three forks offered. Bear selected Fork B.

**Chapters written:** 0 (Fork B explicitly excludes survey-chapter drafting until `book.md` is calibrated and a running project is selected).

**Chapter 00 generated:** `chapters/00-claude-basics.md` — ~6,200 words, workshop Feynman voice, 8-section structure, project-agnostic LLM Exercise (timing wrinkle of Battle of New Orleans / Treaty of Ghent), 2 inline Dig Deeper prompts, quick-reference card, "What would change my mind" + "Still puzzling" tails. Voice flag: `voice-unanchored` — both root `style/` and per-book `style/` were not inspected; first chapter is voice-setting and needs deliberate review.

**Chapter Map produced:** `_chapter-map.md` — all 32 chapters with sections, core concepts, capabilities, vocabulary, and 3–4 Dig-Deeper candidates each. Five LLM-error sites identified for enrichment seeding: Emancipation Proclamation, Battle of New Orleans timing, Compromise of 1877, Philippine-American War, Social Security exclusions. Three source-quality flags raised: Ch 12 misplaced section, Ch 26 thin source extraction, Ch 32 added module beyond OpenStax.

**Running project candidates:** `_running-projects-candidates.md` — four options (Verification Logbook, Counter-Narrative Wiki, Source-Triangulation Agent, Voices Anthology) with adaptability, tool path, Chapter 00 connection, and trade-offs each. Recommended Option 1 (Verification Logbook) as default; recommended Option 4 (Voices Anthology) as instructor swap-in.

**Open decisions surfaced for Bear:**
1. Fill out `book.md` (audience, scope, prerequisites, subtitle).
2. Inspect / populate `style/` directories before survey-chapter drafting.
3. Select one of the four running projects.
4. Decide whether Ch 32's added 2016 module is the endpoint or whether further extension (2020 election, COVID-19) is planned.
5. Move source subfolders out of `chapters/` to `_source/` before drafting begins, so the workshop's `chapters/NAME.md` convention works without confusion.

**Chapter log:**
- `00-claude-basics.md` — ~6,200 words — generated — FLAGGED: voice-unanchored, project specifics deferred to Ch 1.

---

## 2026-05-10 — Voice-matched drafts, batch 1

Bear locked the voice with his rewrite of Chapter 16. His version saved as the canonical Chapter 16 (overwriting my earlier draft). Subsequent chapters drafted to match: prose-style section names (no numbering, no learning-objectives boxes, no Dig Deeper boxes), tighter paragraphs, sparser primary-source linking, "What would change my mind" + "Still puzzling" tails preserved. Each chapter ~3,500–4,500 words, drawn from the OpenStax source in `chapters/[NN-slug]/`.

**Saved in this batch:**

- `chapters/00-claude-basics.md` — rewritten in new voice. ~3,200 words. Dropped Dig Deeper framework, learning-objectives box, suggested-titles list, tags. Kept Battle of New Orleans / Treaty of Ghent hook, LLM-as-confabulator mechanism, three-move discipline (specify / compare / verify), four-running-project preview, LLM Exercise.
- `chapters/2026-05-10-01-the-americas-europe-and-africa-before-1492.md` — Bernal Díaz at Tenochtitlán cold open; specifying "discovery"; mechanism deep-dive on what changes when slavery crosses the Atlantic (racial / hereditary / chattel / scale). LLM Exercise targets pre-1491 population claims.
- `chapters/2026-05-10-02-early-globalization-the-atlantic-world.md` — Las Casas as cold open; the Columbian Exchange as biological event; the labor-substitution mechanism from indigenous to African enslaved labor; the Black Legend framing problem. LLM Exercise targets demographic-catastrophe numbers.
- `chapters/2026-05-10-03-creating-new-social-orders.md` — Bacon's Rebellion as cold open; four colonial systems specified; mechanism deep-dive on the 1640–1705 Virginia statutes that built racial chattel slavery; three regional patterns settled by 1700. LLM Exercise targets the legal-construction-of-race claim.
- `chapters/2026-05-10-04-rule-britannia-the-english-empire.md` — Whitefield and Franklin in Philadelphia as cold open; specifying "British Empire" as four kinds of integration; mechanism deep-dive on sugar and the Caribbean labor economy; the Awakening and Enlightenment as parallel integrators; Seven Years' War as financial origin of the 1760s crisis. LLM Exercise targets the British Caribbean vs. mainland slave-trade asymmetry.
- `chapters/2026-05-10-05-imperial-reforms-and-colonial-protests.md` — Franklin's House of Commons testimony as cold open; specifying what "no taxation without representation" compressed (4 constitutional moves); five-crisis sequence 1763–74; the role of women in non-importation. LLM Exercise targets historiographic interpretations of the Revolution's causes.
- `chapters/2026-05-10-the-era-of-reconstruction.md` — Bear's rewrite, canonical voice exemplar.

**Remaining after batch 1: 26 chapters (6–15, 17–32).**

---

## 2026-05-10 — Voice-matched drafts, batch 2

**Saved in this batch:**

- `chapters/2026-05-10-06-americas-war-for-independence.md` — Dunmore Proclamation as cold open; the war as a civil war among British subjects; four overlapping populations (Patriots, Loyalists, enslaved Africans, Indigenous nations); three-phase military narrative; Black Loyalists to Nova Scotia and Sierra Leone. LLM Exercise targets the elided Black Loyalist material.
- `chapters/2026-05-10-07-creating-republican-governments.md` — Shays' Rebellion → Philadelphia Convention as cold open; Articles of Confederation failure; mechanism deep-dive on the three slavery clauses (Three-Fifths, Slave Trade, Fugitive Slave) and how each operated; Federalist/Anti-Federalist debate; republicanism vs. democracy as framers' explicit position. LLM Exercise targets the Three-Fifths Compromise's actual political function.
- `chapters/2026-05-10-08-growing-pains-the-new-republic.md` — Hamilton's *Report on Public Credit* and the Dinner Table Bargain as cold open; four components of Hamilton's program; the unintended emergence of the party system; Alien and Sedition Acts and the Virginia-Kentucky Resolutions; election of 1800 as first peaceful transfer; Louisiana Purchase as constitutional improvisation; War of 1812 as politically reorganizing event. LLM Exercise targets the Louisiana Purchase as strict-vs-broad-construction test.
- `chapters/2026-05-10-09-industrial-transformation.md` — Lucy Larcom at Lowell as cold open; three waves of industrial transformation (putting-out, factory, deskilling); transportation revolution (canals, railroads); Panic of 1819 and the political-economic populism it produced; class consolidation; the cotton-textile nexus that linked Northern industry to Southern slavery. LLM Exercise targets the North-South economic integration the standard narrative separates.
- `chapters/2026-05-10-10-jacksonian-democracy.md` — Trail of Tears as cold open; the central paradox of expansion-alongside-contraction; institutional democratization of the 1820s–30s; Nullification Crisis as rehearsal for Civil War constitutional argument; Bank War and its century-long financial consequences; what "the people" meant in Jacksonian formulation (about 30% of adults). LLM Exercise targets the simultaneous-expansion-and-contraction framing.

**Remaining after batch 2: 21 chapters (11–15, 17–32).**

---

## 2026-05-10 — Voice-matched drafts, batch 3

**Saved in this batch:**

- `chapters/2026-05-10-11-a-nation-on-the-move.md` — O'Sullivan coining "Manifest Destiny" in *Democratic Review* July 1845 as cold open; the three compressed claims (theological, demographic, racial); the Mexican-American War as a war of choice; the Treaty of Guadalupe Hidalgo's betrayed promises; the California Gold Rush and the California Indigenous genocide. LLM Exercise targets the coinage and political work of the phrase.
- `chapters/2026-05-10-12-cotton-is-king.md` — Hammond's "Cotton is King" Senate speech 1858 as cold open; the financial scale of slavery ($3.5 billion, 20% of US wealth); the four features that made Atlantic chattel slavery a new institution; the internal slave trade as central mechanism; the proslavery shift from "necessary evil" to "positive good." LLM Exercise targets the financialization of enslaved human beings.
- `chapters/2026-05-10-13-antebellum-idealism-and-reform.md` — Seneca Falls Convention 1848 as cold open; Second Great Awakening as engine; abolitionism's transformation from colonization to immediate abolition; Black abolitionists as central rather than auxiliary (per Manisha Sinha); how abolitionism produced organized feminism through the 1840 London convention. LLM Exercise targets the entanglement of abolitionism and feminism.
- `chapters/2026-05-10-14-troubled-times-the-tumultuous-1850s.md` — caning of Sumner May 1856 as cold open; the Compromise of 1850 and its costs; Kansas-Nebraska as the moment the political system broke; *Dred Scott*'s three holdings; John Brown's raid and the 1860 election collapse. LLM Exercise targets *Dred Scott*'s three-part holding (often summarized as one).
- `chapters/2026-05-10-15-the-civil-war.md` — Alexander Stephens's Cornerstone Speech March 1861 as cold open; head-on with the "states' rights" framing (the seceding states' own documents named slavery as the cause); year-by-year military narrative; mechanism deep-dive on what the Emancipation Proclamation actually did (and didn't); wartime federal-government transformation. LLM Exercise targets the Emancipation Proclamation's specific legal content.

**Remaining after batch 3: 16 chapters (17–32).**

---

## 2026-05-10 — Voice-matched drafts, batch 4

**Saved in this batch:**

- `chapters/2026-05-10-17-go-west-young-man.md` — Wounded Knee (Dec 29, 1890) as cold open; the federal-subsidy infrastructure that built the West (Homestead Act, Pacific Railway Acts, Morrill Acts); the federal-government destruction of Indigenous political existence (Army campaigns, bison destruction, Dawes Act, boarding schools); Chinese Exclusion Act; Hispanic dispossession. LLM Exercise targets the Dawes Act as land-transfer mechanism.
- `chapters/2026-05-10-18-industrialization-and-big-business.md` — Carnegie's Bessemer-converter epiphany 1873 as cold open; technical innovations (steel, electric power, telephone); organizational innovations (corporation, trust, holding company); labor conflict and the strike; consumer culture and department stores/mail-order. LLM Exercise targets the three corporate-consolidation forms.
- `chapters/2026-05-10-19-growing-pains-of-urbanization.md` — Jacob Riis's *How the Other Half Lives* 1890 as cold open; demographic transformation (internal migration, Great Migration begins, "new" European immigration); physical city (mass transit, skyscraper, tenement); political machines as service-delivery institutions; settlement house movement and Hull House. LLM Exercise targets the machines beyond the corruption framing.
- `chapters/2026-05-10-20-politics-in-the-gilded-age.md` — Bryan's "Cross of Gold" speech July 1896 as cold open; close-election Third Party System; gold-silver-greenback monetary politics; Populist movement; 1896 as turning-point election. LLM Exercise targets the gold-silver debate as distributional conflict.
- `chapters/2026-05-10-21-leading-the-way-progressive-movement.md` — Triangle Shirtwaist fire March 25, 1911 as cold open; three Progressivisms (efficiency, moral, social-justice) under one label; muckrakers; the Roosevelt-Taft-Wilson presidencies; the Progressive movement's racial-exclusionary commitments. LLM Exercise targets the internal contradictions of the movement.
- `chapters/2026-05-10-22-age-of-empire.md` — Philippine-American War (1899–1913) as central material; Turner-Mahan intellectual case for empire; Spanish-American War and the *Insular Cases*; Philippine-American War's scale (200,000–600,000 Filipino deaths) and contemporary debate; Open Door, Panama Canal, Roosevelt Corollary, Dollar Diplomacy. LLM Exercise targets the elided Philippine-American War.

**Remaining after batch 4: 10 chapters (23–32).**

---

## 2026-05-10 — Voice-matched drafts, batch 5 (final batch)

**Saved in this batch (all 10 remaining):**

- `chapters/2026-05-10-23-americans-and-the-great-war.md` — *Schenck v. United States* and Holmes's reversal at *Abrams* as cold open; path to American belligerence (submarine warfare, Zimmermann telegram, Russian Revolution); the largest civil-liberties contraction (Espionage Act, Sedition Act, Committee on Public Information, APL); Great Migration acceleration and Red Summer of 1919; 1918 influenza pandemic; Versailles and the Senate's rejection.
- `chapters/2026-05-10-24-the-jazz-age.md` — Tulsa Race Massacre 1921 as cold open; the simultaneity of Jazz Age and racial-political violence; uneven 1920s prosperity; Harlem Renaissance; Prohibition, the second Klan, the National Origins Act, the Scopes Trial; the 1929 crash.
- `chapters/2026-05-10-25-brother-can-you-spare-a-dime.md` — Bonus Army attack July 1932 as cold open; the crash that was not the depression; structural causes (monetary contraction, gold standard, Smoot-Hawley); what Hoover did and didn't do; conditions of the Depression; 1932 election.
- `chapters/2026-05-10-26-franklin-roosevelt-and-the-new-deal.md` — Social Security Act's racial exclusions as cold open; First Hundred Days legislation; Second New Deal; court-packing crisis; what the New Deal did not do (anti-lynching, segregation, universal health, full recovery); what it did.
- `chapters/2026-05-10-27-world-war-ii.md` — Hiroshima as cold open with full historiographic spread (Alperovitz / Walker / Hasegawa); path to American entry; wartime federal-government transformation; home front (women, African Americans / Double V, Japanese internment, Bracero, Indigenous service); European theater and Holocaust; Pacific theater and the bombs; post-war American position.
- `chapters/2026-05-10-28-post-war-prosperity-and-cold-war.md` — GI Bill's racial-disparate operation as cold open; institutional infrastructure of the post-war boom; origins of the Cold War with full historiographic spread; Korean War; McCarthyism; early Civil Rights movement and *Brown*.
- `chapters/2026-05-10-29-contesting-futures.md` — Civil Rights Act signing July 1964 with the 75 pens as cold open; LBJ's Great Society legislative wave; Vietnam War; cultural-political transformations (Black Power, women's liberation, gay rights, Native American movement, Chicano movement, counterculture); 1968 collapse.
- `chapters/2026-05-10-30-political-storms.md` — Watergate arrest June 1972 as cold open; Nixon's substantively-not-very-conservative domestic policy; the Southern Strategy with Atwater's 1981 explicit articulation; Vietnam's end; post-Watergate institutional reforms; 1970s economic crisis; Carter administration.
- `chapters/2026-05-10-31-cold-war-to-culture-wars.md` — Fall of the Berlin Wall November 1989 as cold open; Reagan's economic policy and the supply-side empirical record; end of the Cold War; Clinton's Third Way; the 1990s economic boom and globalization; the culture wars.
- `chapters/2026-05-10-32-twenty-first-century.md` — 9/11 as cold open; the post-9/11 wars in Afghanistan and Iraq; 2008 financial crisis and Obama administration; 2016 election; COVID-19 pandemic; January 6, 2021; methodology of teaching recent history while the historiography is still in formation.

**All 32 survey chapters drafted, plus Chapter 00 rewritten. Plus Bear's voice-exemplar Chapter 16 (Reconstruction). Total: 33 chapter drafts.**

---

## Status: First-draft pass complete.

All chapters are first drafts in Bear's voice, drawn from each chapter's OpenStax source. Each chapter opens in a scene with a named actor performing a specific act on a specific date; each has a mechanism deep-dive in the middle; each closes with an LLM Exercise targeting a verifiable claim; each includes "What would change my mind" and "Still puzzling" tails.

Known caveats requiring human review:
- The Ch 17 framing of western settlement as federal-government project is sharper than most textbooks; the substance is supported by current scholarship (Limerick, White) but at variance with popular memory.
- The Ch 21 three-Progressivisms typology is mine, not consensus.
- The Ch 15 head-on rejection of the "states' rights" framing of Civil War causes is correct on the documentary record but sharper than many audiences expect.
- The Ch 24 framing of the Tulsa massacre's erasure is supported by current scholarship but may need patient pull-apart for some readers.
- The Ch 32 explicit acknowledgment that recent historiography is in formation may need adjustment depending on how the book wants to handle contemporary political-cultural questions.
- Across all chapters, the LLM Exercises consistently use the Verification Logbook framing — adjust if a different running project is selected.

Source folders under `chapters/[NN-slug]/` remain in place. Per the earlier _notes-enrichment-pushback.md, these should be moved to `_source/[NN-slug]/` before the chapters/ directory is treated as canonical.
