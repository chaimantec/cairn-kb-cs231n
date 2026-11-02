# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 11–18 — not started. Runs so far have covered lectures 1–10, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 10 — Lecture 10 (Video Understanding), 2026-11-02

Scope: lecture 10 only, video wElqklprhPE (68:45). Guest lecture by Ruohan Gao (introduced at
0:05). One deck, `lecture_10.pdf`: 103 pages, printed 1–103, 1:1 with the PDF; pages 5, 6, 88–91,
93–95 and 100 print no number (labels inferred from neighbours). Title slide "Lecture 10: Video
Understanding", May 1, 2025. Images opted in (every figure-bearing slide), as in runs 1–9. PDFs
link-only. Slug `10-video-understanding`.

#### Transcripts
- [x] 10 Video Understanding — video wElqklprhPE (original captions in raw/transcripts/original/; 89 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_10.pdf (title slide checked); already in sources.md

#### Slides (Step 1b)
- [x] raw/slides/10-video-understanding.md — Sonnet transcription (four agents, pages 1–26 / 27–52 / 53–78 / 79–103, all finished, chunks appended), --verify (103 headings; OK); header by the parent; printed text, tables and chart values checked against the text layer; slide 10 [Ed:] rewritten (the agent called ~1.5 and ~10 GB low; they match binary GB); slide 45's formulas set in LaTeX
- [x] Figure audit (Sonnet), two agents, 39 slides, crops of 600 dpi renders: 13, 14, 23, 25–28, 33, 36–39, 42–48 and 57, 58, 60–62, 70, 71, 73–78, 80–83, 85, 99–101. Corrections: 28 (top dot joins the outer two), 37 (grid 12 x 11, colours), 38 (six labels per frame; red bars on lower predictions), 43 (dot position), 47 (temporal conv2 has no "norm."), 85 (17 frames, not 15), 99 (six MoViNets frames; "Mowing the Lawn"), small additions on 36, 70, 76, 77, 81. Slide 39's C3D bar is in the text layer only (hidden). Parent checked 85 and 76 on the 1400px renders
- [x] Worked arithmetic recomputed, drawn architectures counted, slips kept with [Ed:] lines: 30 (3D CNN GlobalAvgPool "24 x 1 x 1"), 35–37 ("Slide over x and y" on the 3D kernel), 41 ("MFLOPs" holds GFLOPs; FC rows do not recompute), 75 ("copy Kt times in space"). Recomputed and consistent: 10–11 (binary GB, 588 KB), 24–31 (every size and receptive field), 41 (every conv row; 2.9x), 75 (inflation)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/10-video-understanding.md — Sonnet copy-edit; 89/89 markers identical; number diff all listed; ratios 0.69–1.0 (19:24 and 1:01:12 at 0.69 read against the original: stutters only); introduced-word sweep found five unlisted mis-edits, restored by the parent: 39:29→40:17 "exists there temporally" and 59:39→1:00:25 "guess" moved across markers; 47:15 "on top of" inserted; 7:48 "Say we take" for "We made"; 15:33 "go" for "come"; also 1:38 "for each category", 37:12 tense; header coverage times for 1:05–1:08 corrected; pronouns neutral. 5 student-question and 2 student-answer markers; 39 [unclear]

#### Images (Step 1c)
- [x] raw/images/10-video-understanding/ — rendered 47 (31 JPEG, 16 PNG; 6.3 MB); embedded in the slide file (47); header lists every unrendered slide and why (56, checked by script to cover 1–103)
- [x] Embed in the wiki page and topic pages, hand-written captions (lecture page 47, placed by hand with 17 hand-written captions; fourteen `.jpg` links corrected to `.png`; embed script dry run adds nothing; topic page 2: slides 36, 47)
- [x] Look at two rendered images against the slide-file claims (85: 17 frames, boxes on 3–8 and 11–14; 76: every value and both series colours)
- [x] INDEX.md image rules (lectures 1–10; lecture 10 has 47); AGENTS.md table row (47 of 103) and lessons (video stills like animation frames; text layer can hold hidden content; never type an image path; cross-marker moves and quotation checks); BUILD_LOG.md render record; LICENSE.md attribution (lecture 10 table; Layer 2 names the guest lecturer)

#### Wiki
- [x] wiki/10-video-understanding.md (guest lecturer; coverage; every section with slide and timestamp citations; four slips at the end; quotations checked verbatim by script, which found three paraphrased quotes and one transcript substitution)
- [x] Topic pages and cross-links: new wiki/video-understanding.md; sections or bullets in computer-vision-tasks, convolutional-networks (3D convolution section), cnn-architectures, recurrent-neural-networks, attention, transformers, transfer-learning, visualizing-networks, object-detection, course-logistics (row 10; "lectures 1–10"), lecture 9 page (next lecture); every anchor link checked by script
- [x] INDEX.md table of contents (coverage 10 of 18; lecture 10 citation rule, coverage and spoken additions, four slips; lecture 10 and video-understanding entries; nine one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–10"

#### Publish
- [x] kb.json — coverage (10 of 18; 30 topic pages), decks 11/11, figure audit 11/11 (lecture 10 note), images 416 (byLecture 10: 47; 306 JPEG, 110 PNG), caveats for lecture 10's coverage, numbering, slips and 39 unclear marks
- [x] BUILD_LOG.md — lecture 10 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 after converting italic [Ed:] math and slide 100's subscripts, 29 formulas GitHub showed raw, and one INDEX formula after a quote mark; 4,388 formulas render in both; lecture 10 47 on disk / 47 in wiki; numeric claims in INDEX/AGENTS match)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
