# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 12–18 — not started. Runs so far have covered lectures 1–11, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 11 — Lecture 11 (Large-Scale Distributed Training), 2026-11-03

Scope: lecture 11 only, video 9MvD-XsowsE (72:53). One deck, `lecture_11.pdf`: 148 pages, printed
1–148, 1:1 with the PDF, no unnumbered pages. Title slide "Lecture 11: Large-Scale Distributed
Training", May 6, 2025. Images opted in (every figure-bearing slide), as in runs 1–10. PDFs
link-only. Slug `11-large-scale-distributed-training`.

### Transcripts
- [x] 11 Large Scale Distributed Training — video 9MvD-XsowsE (original captions in raw/transcripts/original/; 95 paragraphs)

### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_11.pdf (title slide checked)
- [x] sources.md entry for lecture_11.pdf (already listed by the run 1 crawl)

### Slides (Step 1b)
- [x] raw/slides/11-large-scale-distributed-training.md — Sonnet transcription (four agents, pages 1–37 / 38–74 / 75–111 / 112–148, all finished, chunks appended), --verify (148 headings; OK); header by the parent (coverage and images sections pending); printed numbers and citations checked against the text layer; slide 17 axis "TFLOP/sec"; notation made consistent (slides 71–101 arrows over F; partial-derivative labels; math moved off quote marks); [Ed:] on 139 (Z printed [DxD]); check_math clean
- [x] Figure audit (Sonnet), two agents, 43 slides: A 9, 10, 12, 13, 16, 17, 23, 24, 26, 27, 41, 46, 56, 61–63, 65, 75, 80, 88, 96, 98, 100, 101 (600 dpi crops on the hardware slides, 400 on 61–63, 200–250 dpi views elsewhere); B 105, 106, 109, 112, 113, 116, 117, 120, 123, 124, 130, 131, 133, 136, 139, 140, 143, 146, 147 (600 dpi crops throughout; all clean). Corrections: 17 (no Mar-23 line; point dates; four TC points), 24, 27, 56, 61 (GPU 1 holds W_2), 62; small additions 10, 12, 139 (hidden block labels in the text layer), 146, 147. Parent checked renders of 61 (list text prints plain dL/dW_i: restored on 55–58) and 106 (every point)
- [x] Worked arithmetic recomputed, drawn units counted, slips kept with [Ed:] lines: 25 (1.875 PB is 24,576 x 80 GB in binary units), 68 ("Adam β1, β1"), 69 (63GB is binary), 98 (counter "Current Memory: 2" with one box solid), 139–143 (Z printed [DxD]; Z = YU is N x D). Recomputed and consistent: 14–16, 25's other totals, 44, 68, 125, 130, 133 (16/28), 146 (TP x CP x PP x DP; 16M tokens)

### Transcript edit (Step 1a)
- [x] raw/transcripts/11-large-scale-distributed-training.md — Sonnet copy-edit; 95/95 markers identical; number diff all listed (stutters and false starts at 12:28, 13:13, 13:59, 24:45, 25:32; punctuation elsewhere); ratios 0.75–1.05, no outliers; introduced-word sweep read every paragraph's new words: one broken word fixed by the parent (1:00:49 began "utation"; now "recomp-" / "computation" as the captions split it), one unlisted substitution added to the header (35:29 "lower scale" → "large-scale"); restored names on the slides (GPT-4, Llama, MI325X, Trainium, FSDP, HSDP, Adam, ReLU, QKV, Ulysses) or spoken only (Huang Auditorium, Anthropic, DistributedDataParallel). 13 student-question markers (3 inferred); 5 [unclear]; slides 2 and 148 not presented

### Images (Step 1c)
- [x] raw/images/11-large-scale-distributed-training/ — rendered 30 (13 JPEG, 17 PNG; 4.1 MB); embedded in the slide file (30); header lists every unrendered slide and why (118, checked by script to cover 1–148 with no overlap)
- [x] Embed in the wiki page and topic pages, hand-written captions (lecture page: 30, 29 placed by hand with hand-written captions and one, slide 5, by the script, caption then rewritten; three typed `.png` paths were `.jpg` and were corrected from disk before the script ran; topic page: 1, slide 146)
- [x] Look at two rendered images against the slide-file claims (61: every label, arrow and the overlap text, and the plain dL/dW_i in the list; 106: every point)
- [x] INDEX.md image rules (lectures 1–11; lecture 11 has 30); AGENTS.md table row (30 of 148) and two lessons (slide words against its own drawing; notation pass converts labels, not printed prose); BUILD_LOG.md render record; LICENSE.md attribution (lecture 11 table; Layer 2 decks list)

### Wiki
- [x] wiki/11-large-scale-distributed-training.md (lecturer unnamed; coverage; every section with slide and timestamp citations; slips at the end; 108 quotations checked verbatim by script; check_math clean)
- [x] Topic pages and cross-links: new wiki/distributed-training.md; backpropagation (section on storing or recomputing activations), optimizers, gradient-descent, transformers, attention, language-models, course-logistics (row 11, "lectures 1–11", slide 2's midterm dates), lecture 10 page (next lecture)
- [x] INDEX.md table of contents (coverage 11 of 18; lecture 11 numbering, coverage and spoken additions, eight slips; lecture 11 and distributed-training entries; seven one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–11" and CS336 added

### Publish
- [x] kb.json — coverage (11 of 18; 31 topic pages), decks 12/12, figure audit 12/12 (lecture 11 note), images 446 (byLecture 11: 30; 319 JPEG, 127 PNG), caveats for lecture 11's coverage, numbering, slips and 5 unclear marks
- [x] BUILD_LOG.md — lecture 11 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 once the new pages were staged; 5,004 formulas render in both; lecture 11 30 on disk / 30 in wiki; numeric claims in INDEX/AGENTS match; no ranking claims)
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
