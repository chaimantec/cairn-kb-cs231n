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
- [ ] raw/slides/07-recurrent-neural-networks.md — Sonnet transcription (four agents, pages 1–31 / 32–62 / 63–93 / 94–124), --verify
- [ ] Figure audit (Sonnet), crops of every value checked
- [ ] Worked arithmetic recomputed; printed slips kept with [Ed:] lines

### Transcript edit (Step 1a)
- [ ] raw/transcripts/07-recurrent-neural-networks.md — Sonnet copy-edit; markers, number inventory, word ratios, restored names

### Images (Step 1c)
- [ ] raw/images/07-recurrent-neural-networks/ — render, embed in the slide file; header lists unrendered slides and why
- [ ] Embed in the wiki page and topic pages; hand-written captions
- [ ] Look at two rendered images against the slide-file claims
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
