# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 3–18 — not started. Runs so far have covered lectures 1 and 2, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 2 — Lecture 2 (Image Classification with Linear Classifiers)

Scope: lecture 2 only, video pdqofxJeBN8 (67 min). One deck, `lecture_2.pdf`: 102 pages, printed
1–104, 32 and 49 absent. Images opted in (every figure-bearing slide). PDFs link-only.

#### Transcripts
- [ ] 02 Image Classification with Linear Classifiers — video pdqofxJeBN8 (original captions in raw/transcripts/original/)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_2.pdf (title slide: "Lecture 2: Image Classification with Linear Classifiers", April 3, 2025)

#### Slides (Step 1b)
- [ ] raw/slides/02-image-classification.md — number map, Sonnet transcription, --verify
- [ ] Figure audit (Sonnet, 600 dpi crops) on chart/table/figure pages

#### Transcript edit (Step 1a)
- [ ] raw/transcripts/02-image-classification.md — Sonnet copy-edit; timestamp, number, ratio checks; proper-noun grep

#### Images (Step 1c)
- [ ] raw/images/02-image-classification/ — select, render, embed in slide file and wiki
- [ ] Look at two rendered images against the slide-file claims
- [ ] INDEX.md image rules; AGENTS.md table row; BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [ ] wiki/02-image-classification.md
- [ ] Topic pages (cross-lecture concepts introduced in lecture 2)
- [ ] INDEX.md table of contents

#### Publish
- [ ] kb.json — coverage, images, caveats
- [ ] BUILD_LOG.md — lecture 2 record
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
