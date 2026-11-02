# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 7–18 — not started. Runs so far have covered lectures 1–6, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 6 — Lecture 6 (Training CNNs and CNN Architectures), 2026-11-02

Scope: lecture 6 only, video aVJy4O5TOk8 (71:07). One deck, `lecture_6.pdf`: 97 pages, printed
1–97, 1:1. Title slide "Lecture 6: Training CNNs and CNN Architectures", April 17, 2025; Zane
Durante (introduces himself in the recording). Images opted in (every figure-bearing slide). PDFs
link-only. Slug `06-training-cnns-architectures`.

#### Transcripts
- [x] 06 Training CNNs and CNN Architectures — video aVJy4O5TOk8 (original captions in raw/transcripts/original/; 93 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_6.pdf (title slide checked); already in sources.md

#### Slides (Step 1b)
- [x] raw/slides/06-training-cnns-architectures.md — Sonnet transcription (three agents, pages 1–33 / 34–66 / 67–97, all finished, chunks appended), --verify (97 headings; OK); parent fixed four GitHub-unsafe maths on slides 11 and 27, tidied two transcriber notes (35, 63), added the "Lecture 13" Ed line (78)
- [x] Figure audit (Sonnet), two agents: 11, 12, 16, 27, 28, 32, 35, 41, 46, 49, 53, 57 and 61, 63, 65, 71, 73, 75, 78, 79, 82, 85, 91, 95. Both rendered at 600 dpi but read most pages downscaled (~110–130 dpi); crops of 35, 41, 73 at 300 dpi and 57, 61, 63, 65 at 600 dpi. Corrections: 35 (each VGG stack draws two "3x3 conv, 256" boxes, not three/four), 41 (no blue square on A1), 63 (an inference removed), 73 (four rectangles), 75 (square positions), 78 (8x8 grid; red box position), 79 (red box on the upper 2048 pair only), 95 (grid circles on the flat part and flanks, none at the peak; guide lines in both plots); 32 box positions added. Confirmed: 11 "Statistics calculated per batch" (also text layer), 57 top group "3x3 conv, 64" (600 dpi crop and text layer), every histogram mean/std on 61/63/65, 85's cells. Parent check of slide 35 on its 1400px render agrees with the audit.
- [x] Worked arithmetic recomputed: 28x28 (6), pooling (7), 2^4096 ~ 10^1233 (17), 7x7 receptive field (37–42), 27C^2 vs 49C^2 (43), 10 crops (73) all exact; sqrt(2/4096) = 0.0221 matches the lecturer's spoken "0.022". Printed oddities kept with [Ed:] lines: 11 ("per batch" for N x 1 per-sample statistics), 35 (VGG16/VGG19 stacks draw 15 and 17 weight layers), 57 (last group labelled 64, slides 53–56 print 512), 78–79 ("Lecture 13"; visualizing is lecture 9 in 2025)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/06-training-cnns-architectures.md — Sonnet copy-edit (the agent hit the session limit after writing the whole file and header, before its report); 93/93 markers identical; ratios 0.73–1.03 (0.73 is 1:01:37, the 61-times "say" caption glitch collapsed with an Ed note); number diff: 20:06 "5x" → Phi (listed), 1:01:37 "60" added in the Ed note. Restored names in the slides or the course staff list (Ehsan, Fei-Fei, Zane Durante); LoRA spoken only. 3 [unclear] (17:00, 27:45, 1:01:37 note), 2 "Student, partly audible" (7:48, 8:35)

#### Images (Step 1c)
- [x] raw/images/06-training-cnns-architectures/ — rendered 33 (13 JPEG, 20 PNG; 3.9 MB); embedded in the slide file (33); header lists every unrendered slide and why
- [x] Embed in the wiki page (33, all with hand-written captions; slide 85 moved below its table) and nine topic pages (31: cnn-architectures 8, normalization-layers 2, weight-initialization 3, data-augmentation 5, transfer-learning 4, regularization 3, hyperparameters 4, imagenet 1, k-NN 1), captions taken from the lecture page
- [x] Look at two rendered images against the slide-file claims (slide 35 diagram: agrees with the audit, two 256 boxes per VGG stack; slide 32 chart: values, boxes and triangles as the file says)
- [x] INDEX.md image rules (lectures 1–6; lecture 6 has 33); AGENTS.md table row (33 of 97); BUILD_LOG.md render record; LICENSE.md attribution (lecture 6 table and not-rendered note)

#### Wiki
- [x] wiki/06-training-cnns-architectures.md (four printed oddities noted: 11, 35, 57, 78–79; slide 2 slide-only; the 51:34 detour and the LoRA / paired-convolution answers marked; slide 19's keep-probability p vs. the spoken "probability of dropout"; the spoken "loss" for the accuracy curves)
- [x] Topic pages cnn-architectures, normalization-layers, weight-initialization, data-augmentation, transfer-learning; sections or links in regularization (dropout, the randomness pattern), neural-networks (lecture 6 activations), hyperparameters-and-validation (lecture 6 section), imagenet, convolutional-networks ("not yet in this knowledge base" replaced), k-nearest-neighbors, image-classification, course-logistics (row 6; stale "lectures 1–4" fixed), lecture 5 page
- [x] INDEX.md table of contents (coverage 6 of 18; lecture 6 citation rule, skipped slide, four oddities; lecture 6 and five topic entries; seven one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–6"

#### Publish
- [x] kb.json — coverage (6 of 18; 20 topic pages), decks 7/7, figure audit 7/7 (lecture 6 note), images 250 (byLecture 6: 33; 193 JPEG, 57 PNG), caveats for lecture 6's coverage, numbering, oddities and unclear marks
- [x] BUILD_LOG.md — lecture 6 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 after fixing six GitHub math problems the --github pass found: two inline maths wrapped across a line break, a `$...$` followed by ")", `x < 0` and two `\,` in the slide file; 2,055 formulas render in both; numeric claims in INDEX/AGENTS match the measured table, lecture 6 33 on disk / 33 in wiki; AGENTS.md gains one general lesson: count drawn architectures box by box)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
