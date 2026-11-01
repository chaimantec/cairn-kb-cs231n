# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 4–18 — not started. Runs so far have covered lectures 1–3, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 3 — Lecture 3 (Regularization and Optimization), 2026-11-02

Scope: lecture 3 only, video dyNGd06MWn4 (68:39). One deck, `lecture_3.pdf`: 119 pages, printed
1–123, 10–12 and 29 absent (hidden slides; raw footer spans confirm, every page reads a printed
number, sequence monotonic). Images opted in (every figure-bearing slide). PDFs link-only.
Slug `03-regularization-optimization`.

#### Transcripts
- [x] 03 Regularization and Optimization — video dyNGd06MWn4 (original captions in raw/transcripts/original/)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_3.pdf (title slide: "Lecture 3: Regularization and Optimization", April 8, 2025)

#### Slides (Step 1b)
- [x] raw/slides/03-regularization-optimization.md — number map, Sonnet transcription (three agents, pages 1–40 / 41–80 / 81–119; the first stopped at slide 40 and was resumed to append 41–44), --verify (119 headings; exit 0); 15 GitHub italics warnings fixed
- [x] Figure audit (Sonnet, 600 dpi crops) on 19 slides: 13, 18, 27, 34, 41, 55, 57, 61, 70, 75, 80, 83, 84, 86, 89, 99, 109, 119, 122 → errors on 80 (wd and L2 values at epochs 6 and 15; L2 above wd at 2 and 6), 84 (plateau levels 1.4 and 1.1, not 1.3 and 1.0), 99 (red points right of the θ axis, not left; 15 blue points, not 17); small omissions on 13 and 122 (bold correct-class scores) and 86 (zero loss at 250–260); trajectory-free heat-maps on 61, 70, 75, 109 confirmed. Fixes applied.

#### Transcript edit (Step 1a)
- [x] raw/transcripts/03-regularization-optimization.md — Sonnet copy-edit; 90/90 markers identical; ratios 0.80–0.97; number diff: only "beta one, beta two" → beta1, beta2 (listed); no number lost. Restored terms all on the slides or in the captions ("llama" at [57:41]); Nesterov, AdaGrad, L-BFGS appear only in the header's coverage note. 26 student-turn markers and 3 [unclear] flags, all matching the header. Recording covers slides 5–99 and ends at 1:08:25; slides 2–4 and 100–123 are slide-file-only.

#### Images (Step 1c)
- [x] raw/images/03-regularization-optimization/ — select, render, embed in slide file and wiki (24 rendered, 2.8 MB, 17 JPEG + 7 PNG; all 24 in the lecture page; 19 on topic pages)
- [x] Look at two rendered images against the slide-file claims (slide 88 inverse-sqrt curve and slide 104 momentum vs. Nesterov diagram, neither in the audit sample: both agree)
- [x] INDEX.md image rules; AGENTS.md table row (and two general lessons: animation frames; range expansion and colon-before-formula in the embed script); BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [x] wiki/03-regularization-optimization.md (24 images via the embed script, 20 hand-written captions; slide 34 truncation, slide 119 base-10 log noted; appendix and slides 100–101 marked slide-only; trajectory-free animation slides explained)
- [x] Topic pages (cross-lecture concepts introduced in lecture 3): regularization, gradient-descent, optimizers, learning-rate-schedules (19 images via --deck-label "Lecture 3", captions reused); links from linear-classifiers, loss-functions, hyperparameters-and-validation, 02-image-classification and the course-logistics roadmap (rows 2 and 3 now linked)
- [x] INDEX.md table of contents (coverage 3 of 18; lecture 3 citation rule; slide-only appendix; missing animations)

#### Publish
- [x] kb.json — coverage (3 of 18; 12 topic pages), decks 4/4, figure audit 4/4, images 129 (byLecture 3: 24; 115 JPEG, 14 PNG), caveats for lecture 3 coverage, animations, slips
- [x] BUILD_LOG.md — lecture 3 record
- [x] verify_kb.py clean, and its review section read (exit 0; one inline formula GitHub left as raw text, "(O(n^3))" in parentheses, rephrased; image and page counts in INDEX/AGENTS match the measured table; AGENTS range-expansion sentence corrected to "up to 12 slides")
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
