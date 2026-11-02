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
- [ ] raw/slides/06-training-cnns-architectures.md — Sonnet transcription, --verify
- [ ] Figure audit (Sonnet)
- [ ] Worked arithmetic recomputed; printed slips kept with [Ed:] lines

#### Transcript edit (Step 1a)
- [ ] raw/transcripts/06-training-cnns-architectures.md — Sonnet copy-edit; marker, number and ratio checks in the parent

#### Images (Step 1c)
- [ ] raw/images/06-training-cnns-architectures/ — select, render, embed in slide file
- [ ] Embed in the wiki page and topic pages; hand-written captions
- [ ] Look at two rendered images against the slide-file claims
- [ ] INDEX.md image rules; AGENTS.md table row; BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [ ] wiki/06-training-cnns-architectures.md
- [ ] Topic pages and cross-links
- [ ] INDEX.md table of contents; SEE_ALSO coverage line

#### Publish
- [ ] kb.json
- [ ] BUILD_LOG.md — lecture 6 record and index row
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
