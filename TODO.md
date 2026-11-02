# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 10–18 — not started. Runs so far have covered lectures 1–9, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 9 — Lecture 9 (Detection, Segmentation, Visualization, and Understanding), 2026-11-02

Scope: lecture 9 only, video PTypu6GqEd4 (73:43). One deck, `lecture_9.pdf`: 178 pages, printed
1–178, 1:1 with the PDF (no hidden slides, no unnumbered pages). Title slide "Lecture 9:
Detection, Segmentation, Visualization, and Understanding", April 29, 2025. Images opted in
(every figure-bearing slide). PDFs link-only. Slug `09-detection-segmentation-visualization`.

### Transcripts
- [x] 09 Detection, Segmentation, Visualization, and Understanding — video PTypu6GqEd4 (original captions in raw/transcripts/original/; 95 paragraphs)

### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_9.pdf (title slide checked); already in sources.md

### Slides (Step 1b)
- [x] raw/slides/09-detection-segmentation-visualization.md — Sonnet transcription (six agents, pages 1–30 / 31–60 / 61–90 / 91–120 / 121–150 / 151–178, all finished, chunks appended), --verify (178 headings; OK); header written by the parent; slide 127 [Ed:] arithmetic corrected (agent wrote 61.35; it is 60.75, the bias omitted); 3 formulas rewritten with `\ast` for GitHub (check_math clean, 206 formulas)
- [x] Figure audit (Sonnet), two agents, 37 slides: 3, 4, 22, 43, 45, 46, 58, 60, 61, 64, 68, 93, 95, 96, 97, 99, 100 and 107, 112, 115, 116, 117, 120, 121, 127, 139, 140, 145, 146, 147, 152, 156, 158, 163, 165, 169, 176; 600 dpi renders, crops of every value on 3, 43, 60, 61, 64, 107, 127, 139, 140, 145, 146, 147, 163, 176 (half-page crops on the rest of A; B checked 115–121, 152, 156, 158, 165, 169 from whole-page views only). Corrections: 3 (4 encoder and 4 decoder bars), 43 and 64 (right high-res group 2 slabs, not 3), 60–61 (3 bars per U-Net level, concatenated bars half white; "white background" is not a difference), 96 (cyan box overlaps the anchor, not inside), 97 (four anchor shapes), 107 (dashed "no object" curves from black, blue and gold; no lines from pink and yellow), 127 (Ed arithmetic), additions on 146, 147, 176. Parent checked 165 and 60 on the 1400px renders
- [x] Worked arithmetic and drawn architectures recomputed / counted: 25 (8D² both), 46 (max pool and unpool), 72 (4 and 12 numbers), 151–152 (matrix products), 176 (every ReLU cell); blocks counted on 3, 43, 64, 60–61. Slips kept with [Ed:] lines: 3 (x0, x1, x2, x2), 4 (O(N) memory, lecture 8 slide 82), 21 ("identify"), 23 (RMSNorm N vs D), 43 ("Low-res: D3 x H/4 x W/4", repeated on 44 and 59), 127 (61.95 omits the bias; 60.75)

### Transcript edit (Step 1a)
- [x] raw/transcripts/09-detection-segmentation-visualization.md — Sonnet copy-edit; 95/95 markers identical; ratios 0.77–1.00; number diff all listed; an introduced-word sweep found five unlisted mis-edits, all restored by the parent: 11:51 "a few of those experts" (captions "a of those e experts" = slide 27's A of E), 14:57 "overfit" (said "over fine-tune"), 22:38 "a reverse of pooling, unpooling" (now [unclear: uppooling]), 23:25 "train or" dropped, 14:09 and 53:37 inserted words; 11:03 "8 D divided by 3" reverted to "8 divided by 3" (the "di" may be a stutter); header coverage corrected (31:08 backup slides = 151–152; transposed convolution walked through at 26:31–28:49), pronouns neutral. 22 student-question markers (4 inferred), 1 student answer; 10 [unclear] (8 by the editor, 2 by the parent at 22:38)

### Images (Step 1c)
- [x] raw/images/09-detection-segmentation-visualization/ — rendered 53 (48 JPEG, 5 PNG; 7.5 MB); embedded in the slide file (53); header lists every unrendered slide and why (125, checked by script to cover 1–178)
- [x] Embed in the wiki page (53, plus lecture 8 slide 112 and lecture 1 part 2 slide 14 reused by hand) and topic pages (8: image segmentation 3, object detection 3, visualizing networks 2), hand-written captions
- [x] Look at two rendered images against the slide-file claims (165 bar charts: every value; 60 U-Net: three bars per level and the half-white concatenated bars, as corrected)
- [x] INDEX.md image rules (lectures 1–9; lecture 9 has 53); AGENTS.md table row (53 of 178) and two general lessons (sweep the words a transcript edit introduced; another lecture's slide citations anchor the embed script); BUILD_LOG.md render record; LICENSE.md attribution (lecture 9 table and not-rendered note; decks-checked sentence)

### Wiki
- [x] wiki/09-detection-segmentation-visualization.md (lecturer unnamed, refers to "Justin"; coverage with the unpresented Additional Reading Material as its own sections marked slides only; six slips; the tweaks walked through; the per-pixel loss and DETR Q&A spoken only; the lecturer's "R-CNN and Mask R-CNN" at 43:31 before Mask R-CNN is presented; 53 lecture 9 images, 3, 12, 43 and 139 placed by hand, the script's 49 others reviewed and 12 moved (citations of other lectures' slides 60, 78, 100–109 and 112 had pulled 60, 78, 100, 104, 106, 107, 112 into the overview and recap; 158, 163, 164, 165 and 176 sat between a sentence and its formula or table); 21 hand-written captions; lecture 8 slide 112 and lecture 1 part 2 slide 14 images reused by hand)
- [x] Topic pages image-segmentation, object-detection, visualizing-networks; sections or links in computer-vision-tasks (sources, tasks, visualization), transformers (class-token ViT; tweaks walked through; lecture 9 bullet), attention, convolutional-networks (lecture 9 filters; lectures list), normalization-layers (spoken argument), linear-classifiers, loss-functions (per-pixel, multitask), backpropagation, transfer-learning, course-logistics (row 9; "lectures 1–9"), lecture 8 page (tweaks walked through in lecture 9; next lecture), lecture 6 page ("Lecture 13" pointer → lecture 9). Every wiki anchor link checked by script
- [x] INDEX.md table of contents (coverage 9 of 18; lecture 9 citation rule, skipped slides and spoken additions, six slips; lecture 9 and three topic entries; eight one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–9"

### Publish
- [x] kb.json — coverage (9 of 18; 29 topic pages), decks 10/10, figure audit 10/10 (lecture 9 note), images 369 (byLecture 9: 53; 275 JPEG, 94 PNG), caveats for lecture 9's coverage, numbering, slips and unclear marks; lecture 8 caveat notes lecture 9 walks through the tweaks
- [x] BUILD_LOG.md — lecture 9 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 after code-spanning two run 7–8 formula mentions in BUILD_LOG that GitHub showed as raw text, and the `\ast` mentions; 4,132 formulas render in both; numeric claims in INDEX/AGENTS match the measured table, lecture 9 53 on disk / 53 in wiki)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
