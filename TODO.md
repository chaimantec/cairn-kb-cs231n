# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 6–18 — not started. Runs so far have covered lectures 1–5, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 5 — Lecture 5 (Image Classification with CNNs), 2026-11-02

Scope: lecture 5 only, video f3g1zGdxptI (68:04). One deck, `lecture_5.pdf`: 141 pages, printed
1–141, 1:1 (every page prints its number; no gaps). Justin Johnson per the schedule and the
recording. Images opted in (every figure-bearing slide). PDFs link-only.
Slug `05-image-classification-cnns`.

#### Transcripts
- [x] 05 Image Classification with CNNs — video f3g1zGdxptI (original captions in raw/transcripts/original/; 89 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_5.pdf (title slide: "Lecture 5: Image Classification with CNNs", April 15, 2025); already in sources.md

#### Slides (Step 1b)
- [x] raw/slides/05-image-classification-cnns.md — Sonnet transcription (four agents, pages 1–36 / 37–71 / 72–106 / 107–141), --verify (141 headings; OK); 20 inline-math-after-quote warnings and 4 others fixed
- [x] Figure audit (Sonnet), two agents: 4, 6, 22, 24, 26, 34, 35, 38, 62, 69, 80, 81 and 94, 101, 102, 108, 113, 118, 120, 124, 127, 129, 133, 136. Both viewed at ~200 dpi effective (600 dpi renders downscaled by the viewer); B cropped at 600 dpi on 127, 129, 133; A made no crops. Errors on 4 (timeline extents and marks), 22 (bin 5 colour, bar 7 height), 24 (which bars are tall), 81 (blue squares do not overlap; all square positions), small fixes on 35 (one confidence blurry: 0.982 or 0.987), 38, 80, 108, 136 (decoder runs upward). Confirmed: 6's matrices and printed 61.95; 62's K_w x K_h order; 101's swapped labels; 124's "Conv layer" wording; 127's numbers; 129's minus signs (600 dpi crop). Fixes applied.
- [x] Worked arithmetic recomputed: HoG 10,800 (23), 28 and 24 (56, 64), 5x5 (75), 3x3 (86), 32 (89), 76 and 760 (91), 768K (93), 28x28x5 (118), 1216 (127), 6/8/3/4 max pool (102, 122) all exact. Printed slips kept with [Ed:] lines: 6 (ship score omits the bias, as lecture 2 slide 60), 101 (cube labels swapped), 124 ("Conv layer" under the pooling heading), 129 (minus signs in the softmax exponents)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/05-image-classification-cnns.md — Sonnet copy-edit; 89/89 markers identical; ratios 0.80–1.02; number diff traced in full (30:42 false-start "3" and "372" dropped; 49:56 and 54:31 counts written as words; 56:51 "2k + one" → 2K plus 1; 59:56 "64x12 x112", "112 x12" ×2, "224 x24" → 112/224, the captions dropping a digit after "x"; 1:00:44 and 1:02:15 "2x two" → 2 by 2, false-start "two" dropped). Parent fixes: 30:42 "vector" had become "tensor" (reverted); 56:51 "multiply" guess → [unclear: multiple]; 57:38 → [unclear: it's a lot seven]; header listed no digit restorations and had no coverage (both written). Restored names in the slides or the captions (LeNet as "lenat", COVID as "co" in a 2020 aside, Inception, Stable Diffusion, MATLAB, FLOPs, aspect ratio bucketing all in the captions). 19 student-question and 6 student-answer markers, 5 [unclear]. Recording skips slides 2–3 and the appendix 109–141; ends 1:07:34 at slides 107–108.

#### Images (Step 1c)
- [x] raw/images/05-image-classification-cnns/ — select, render (53; 5.8 MB; 34 JPEG, 19 PNG), embed in slide file (53); header lists every unrendered slide and why
- [x] Embed in the wiki page (53, all with hand-written captions; slide 75 moved below its formula) and the convolutional-networks topic page (8: 62, 65, 81, 102, 106, 68 placed in the script's format); dimensions as inline math in prose and plain "5x5x3" in captions; unescaped digit asterisks (5*5*3) escaped in the page, the topic page and the slide file
- [x] Look at two rendered images against the slide-file claims (slide 101: labels swapped as the Ed line says; slide 81: square positions as corrected by the audit, except the second blue cell, which is row 6 column 6, not column 5 — fixed)
- [x] INDEX.md image rules (lectures 1–5; lecture 5 has 53); AGENTS.md table row (53 of 141); BUILD_LOG.md render record; LICENSE.md attribution (lecture 5 table and not-rendered note)

#### Wiki
- [x] wiki/05-image-classification-cnns.md (slips on slides 6, 101, 124 and 129 noted; slides 2–3 and the appendix 109–141 marked slide-only; slide 108's diagrams described unnamed, the transcriber's "inception-style"/"residual-style" glosses removed from the slide file)
- [x] Topic page convolutional-networks; links from neural-networks, image-classification (new section on hand-designed features), hyperparameters-and-validation (lecture 5 section), linear-classifiers, loss-functions (slide 129 slip), optimizers (Adam Test of Time aside), imagenet, computer-vision-tasks, the 01 and 04 pages, and the course-logistics roadmap (row 5)
- [x] INDEX.md table of contents (coverage 5 of 18; lecture 5 citation rule, skipped slides, four slips, slide 8's animation frame; lecture 5 and convolutional-networks entries; image-classification and hyperparameters one-liners; raw-materials lines); SEE_ALSO's "lectures 1–4" → 1–5

#### Publish
- [x] kb.json — coverage (5 of 18; 15 topic pages), decks 6/6, figure audit 6/6 (with lecture 5's ~200 dpi note), images 217 (byLecture 5: 53; 180 JPEG, 37 PNG), caveats for lecture 5's coverage, notation, numbering, slips and unclear marks
- [x] BUILD_LOG.md — lecture 5 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0; all 1,857 formulas render in the chat and on github.com after joining six inline formulas that wrapped across a line break, which only the --github pass caught, and fixing slide-62's extension on the topic page; numeric claims in INDEX/AGENTS match the measured table, lecture 5 53 on disk / 53 in wiki; AGENTS.md gains three general lessons: wrapped inline math, shape notation and digit asterisks; audit renders shown downscaled)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
