# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 8–18 — not started. Runs so far have covered lectures 1–7, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 7 — Lecture 7 (Recurrent Neural Networks)

Scope: lecture 7 only, video kG2lAPBF7zA (71:48). One deck, `lecture_7.pdf`: 124 pages, printed
1–133; hidden 19, 20, 52, 53, 71, 72, 73, 100, 103; page 118 prints no number (127, between 126
and 128). Title slide "Lecture 7: Recurrent Neural Networks", April 22, 2025. Images opted in
(every figure-bearing slide). PDFs link-only. Slug `07-recurrent-neural-networks`.

### Transcripts
- [x] 07 Recurrent Neural Networks — video kG2lAPBF7zA (original captions in raw/transcripts/original/; 93 paragraphs)

### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_7.pdf (title slide checked); already in sources.md

### Slides (Step 1b)
- [x] raw/slides/07-recurrent-neural-networks.md — Sonnet transcription (four agents, pages 1–31 / 32–62 / 63–93 / 94–124, all finished, chunks appended), --verify (124 headings; OK)
- [x] Figure audit (Sonnet), two agents, 27 slides: 7, 12, 23, 33, 54, 56, 58, 61, 62, 64, 65, 66 and 67, 85, 88, 91, 97, 98, 99, 104, 111, 113, 116, 120, 125, 129, 131; 600 dpi crops of every number checked (23, 33, 54, 56, 58, 97, 98, 104 from ~150 dpi page views). Corrections: 7 (two start values), 58 (grey box includes the output), 61 (label colour), 88 (20 boxes, 10 conv, 13 weight layers; the transcriber listed 10 but counted 8), 131 (a missing Pythia point). Confirmed: every vector on 61–66, slide 67's listing values (the transcriber's summary was unverified until cropped), 111's lowercase t, 116's code (no sqrt), 129's "3x3 conv, 64". Parent checked slides 65 and 66 on their 1400px renders: the slips are printed.
- [x] Worked arithmetic recomputed: the repeated-1s RNN (29–38) and slide 65 columns 3–4 exact. Slips kept with [Ed:] lines: 65 (softmax columns 1–2 misplaced: printed (.03,.84,.00,.13) and (.25,.20,.50,.05), scores give (.04,.13,.00,.84) and (.25,.20,.06,.50); the lecturer acknowledges it at 38:42 and 43:21), 66 (w14 in rows 2–3), 106 (W_xh then W_hx), 110 (lowercase t in the chain), 116 (squared norm called the norm), 129 (ResNet's last stage "3x3 conv, 64", as lecture 6 slide 57)

### Transcript edit (Step 1a)
- [x] raw/transcripts/07-recurrent-neural-networks.md — Sonnet copy-edit; 93/93 markers identical; ratios 0.76–1.02; number diff: 13:15 "10h" → tanh, 15:36 "001" → "0 0 1", 17:08 "one" → "1" (all listed), 45:39 "minus one" → "minus 1" twice (unlisted; reverted by the parent). Restored names on the slides, course staff, or spoken-only (TensorBoard, RoPE, beam search); the parent corrected three header claims (Karpathy is on slides 67–68; "four gates"/"gate gate" are on 119 and 121–124). 13 student-question, 2 student-answer, 5 partly-audible markers; 3 [unclear]

### Images (Step 1c)
- [x] raw/images/07-recurrent-neural-networks/ — rendered 43 (29 JPEG, 14 PNG; 5.0 MB); embedded in the slide file (43); header lists every unrendered slide and why (81)
- [ ] Embed in the wiki page and topic pages; hand-written captions
- [x] Look at two rendered images against the slide-file claims (slide 65 chart-like table: softmax values as printed, slips confirmed; slide 66 diagram: w14 rows, embedding layer, as the file says)
- [ ] INDEX.md image rules; AGENTS.md table row; BUILD_LOG.md render record; LICENSE.md attribution

### Wiki
- [ ] wiki/07-recurrent-neural-networks.md
- [ ] Topic pages and cross-links
- [ ] INDEX.md table of contents (coverage 7 of 18); SEE_ALSO

### Publish
- [ ] kb.json — coverage, decks, figure audit, images, caveats
- [ ] BUILD_LOG.md — lecture 7 record and index row
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
