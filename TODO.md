# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 13–18 — not started. Runs so far have covered lectures 1–12, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 12 — Lecture 12 (Self-Supervised Learning), 2026-11-03

Scope: lecture 12 only, video 4howBU7THbM (74:42). One deck, `lecture_12.pdf`: 115 pages,
printed 1–117 with 112 and 113 absent (pages 112–115 = slides 114–117, an appendix after slide
111 "Next time"); every page prints its number. Title slide "Lecture 12: Self-Supervised
Learning", May 8, 2025. Images opted in (every figure-bearing slide), as in runs 1–11. PDFs
link-only. Slug `12-self-supervised-learning`.

#### Transcripts
- [x] 12 Self-Supervised Learning — video 4howBU7THbM (original captions in raw/transcripts/original/; 96 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_12.pdf (title slide checked)
- [x] sources.md entry for lecture_12.pdf (already listed by the run 1 crawl)

#### Slides (Step 1b)
- [x] raw/slides/12-self-supervised-learning.md — Sonnet transcription (three agents, pages 1–38 / 39–76 / 77–115, all finished, chunks appended), --verify (115 headings; OK); header by the parent; credit lines checked against the text layer (all present; 79–80 inherit 78's as builds); quoted math moved off quote marks, `}_ {` subscripts; transcriber glosses removed (5 "occlusion-style", 40 "thylacine-like", 106 "DINOv2 caption"); check_math clean
- [x] Figure audit (Sonnet), two agents, 43 slides, 600 dpi crops throughout: A 22, 23, 27, 31, 33, 39, 59, 60, 78, 83, 84, 85, 86, 89, 91, 92, 93, 100, 102, 105, 114 (corrections on 22, 39, 59, 89, 91, 100, a note on 86; slide 31's bracket confirmed; every table cell and both code listings agree); B 5, 8, 12, 16, 24, 26, 29, 37, 44, 45, 52, 53, 58, 81, 82, 87, 95, 101, 104, 106, 115, 116 (corrections on 8, 16, 24, 26, 37, 45, 53, 101, 106, 115, 116). Parent checked renders of 39 (every curve) and 53 (every count)
- [x] Worked arithmetic recomputed, drawn units counted, slips kept with [Ed:] lines: 31 (unbalanced brackets in L_adv), 81 (10 vectors drawn, 6 x 6 affinity matrix); typos 13, 54; 106 credit names DINO; 53 masks 17 of 25; tables from different papers differ (23/27/33). Recomputed and consistent: 59, 60/102, 91/92, 71/75/107, 78, 2

#### Transcript edit (Step 1a)
- [x] raw/transcripts/12-self-supervised-learning.md — Sonnet copy-edit; 96/96 markers identical; number diff only 18:03 "C410" → CIFAR10 and 25:01 "6064" → 64 (false start), both listed; one ratio outlier, 28:08 at 0.71 (stutters only, read); introduced-word sweep read every paragraph's new words: one substitution reverted by the parent (45:15 "perturbations", a correctly heard caption word, had become "permutations"); two header notes corrected (t-SNE is printed on slide 13; Grad-CAM is lecture 9's); restored names on the slides or spoken only (Grad-CAM, Kinect, Yosemite, Half Dome). 8 student-turn markers; 9 [unclear]; slides 2, 94–111 and 114–117 not presented

#### Images (Step 1c)
- [x] raw/images/12-self-supervised-learning/ — rendered 60 (58 JPEG, 2 PNG; 7.8 MB); embedded in the slide file (60); header lists every unrendered slide and why (55, checked by script to cover all 115 with no overlap)
- [x] Embed in the wiki page and topic pages, hand-written captions (lecture page: all 60 placed by the script, every caption then hand-written; four that first anchored in the overview (94 on "slides 94–111", 115–117 on "slides 114–117") were removed, the overview reworded and the script re-run; four citations moved off formula-introducing paragraphs (76, 88, 98, 104) before the run. Topic page: 10 by the script with --deck-label "Lecture 12" (9, 12, 53, 58, 66, 85, 86, 88, 103, 104), captions copied from the lecture page; two hand-typed image paths removed first and the table's slide ranges turned into section links so it does not collect 40 images)
- [x] Look at two rendered images against the slide-file claims (39: every curve after the audit's corrections; 53: every count)
- [x] INDEX.md image rules (lectures 1–12; lecture 12 has 60); AGENTS.md table row (60 of 115) and three lessons (a long range anchors its first slide, and the opening source line counts as overview; topic-page tables of slide ranges collect images, so link sections; a correctly heard caption word changed to the expected one is a substitution); BUILD_LOG.md render record; LICENSE.md attribution (lecture 12 table; Layer 2 decks list)

#### Wiki
- [x] wiki/12-self-supervised-learning.md (lecturer unnamed; coverage; every section with slide and timestamp citations; slides-only section for CPC onward; slips at the end; 153 quotations checked verbatim by script; check_math clean)
- [x] Topic pages and cross-links: new wiki/self-supervised-learning.md (two tables: pretext tasks; contrastive methods by where negatives come from); course-logistics (row 12, "lectures 1–12", slide 2's midterm times and proposal feedback), lecture 11 page (next lecture), transfer-learning, loss-functions (InfoNCE as N-way cross-entropy), data-augmentation, transformers, visualizing-networks, video-understanding, computer-vision-tasks, attention, distributed-training, lecture 1 page
- [x] INDEX.md table of contents (coverage 12 of 18; lecture 12 numbering, coverage and spoken additions, two slips; lecture 12 and self-supervised-learning entries; nine one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–12"

#### Publish
- [x] kb.json — coverage (12 of 18; 32 topic pages), decks 13/13, figure audit 13/13 (lecture 12 note), images 506 (byLecture 12: 60; 377 JPEG, 129 PNG), caveats for lecture 12's coverage, numbering, slips and 9 unclear marks
- [x] BUILD_LOG.md — lecture 12 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 with the new pages staged; 5,352 formulas render in the chat and on github.com; lecture 12 60 on disk / 60 in wiki; numeric claims in INDEX/AGENTS read and match; stale "1–11" / "12–18" wording grepped: only the open lectures line, narrowed to 13–18)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
