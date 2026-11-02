# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 9–18 — not started. Runs so far have covered lectures 1–8, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 8 — Lecture 8 (Attention and Transformers)

Scope: lecture 8 only, video RQowiOF_FvQ (66:31). One deck, `lecture_8.pdf`: 122 pages, printed
1–122, 1:1 with the PDF (no hidden slides, no unnumbered pages). Title slide "Lecture 8: Attention
and Transformers", April 24, 2025. Images opted in (every figure-bearing slide). PDFs link-only.
Slug `08-attention-transformers`. The recording leaves "Tweaking Transformers" (110–120) "as extra
reading" (≈1:05:22).

#### Transcripts
- [x] 08 Attention and Transformers — video RQowiOF_FvQ (original captions in raw/transcripts/original/; 87 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_8.pdf (title slide checked); already in sources.md

#### Slides (Step 1b)
- [ ] raw/slides/08-attention-transformers.md — Sonnet transcription (four agents), --verify
- [ ] Figure audit (Sonnet), crops of every value checked
- [ ] Worked arithmetic and drawn architectures recomputed / counted

#### Transcript edit (Step 1a)
- [ ] raw/transcripts/08-attention-transformers.md — Sonnet copy-edit; markers, numbers, ratios, proper nouns

#### Images (Step 1c)
- [ ] raw/images/08-attention-transformers/ — render, embed in the slide file, header lists unrendered slides
- [ ] Embed in the wiki page and topic pages; hand-written captions
- [ ] Look at two rendered images against the slide-file claims
- [ ] INDEX.md image rules; AGENTS.md table row; BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [ ] wiki/08-attention-transformers.md
- [ ] Topic pages and cross-links
- [ ] INDEX.md table of contents; SEE_ALSO

#### Publish
- [ ] kb.json — coverage, images, caveats
- [ ] BUILD_LOG.md — lecture 8 record and index row
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
