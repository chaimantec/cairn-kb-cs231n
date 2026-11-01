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
- [x] 02 Image Classification with Linear Classifiers — video pdqofxJeBN8 (original captions in raw/transcripts/original/)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_2.pdf (title slide: "Lecture 2: Image Classification with Linear Classifiers", April 3, 2025)

#### Slides (Step 1b)
- [x] raw/slides/02-image-classification.md — number map, Sonnet transcription (three agents, pages 1–34 / 35–68 / 69–102), --verify (102 headings; exit 0). slide_number_map.py patched: page 32's "33" overlaps the "Lecture 2 -" box, so the split-footer test missed it and the corner fallback read a "1" subscript from the page's equations; all 541 decks on disk otherwise map identically.
- [x] Figure audit (Sonnet, 600 dpi crops) on 14 slides: 8, 23, 30, 33, 45, 57, 60, 62, 63, 64, 65, 74, 94, 101 → 8 clean; errors on 8 (pixel array "not transcribed, tiny" was legible: 24×16, not ~20×15), 33 (L1 path drawn up-then-right, not right-then-up), 64 (third circle left of the axis, not right); loose detail on 30, 45 (means per k now tabulated), 63. Fixes applied.

#### Transcript edit (Step 1a)
- [x] raw/transcripts/02-image-classification.md — Sonnet copy-edit; 87/87 markers identical; ratios 0.74–1.00; number diff all deliberate (01 → O(1); "20 five" → [Ed: 25]; 372 → [Ed: 3072] ×3; "2x two" → 2x2; C4 → CIFAR-10; CS2 229 → CS 229). Parent reverted one interpretive insertion at [34:51] ("there" → "with L2"). Restored terms all on the slides except GPT (in the captions). Recording covers slides 5–83 and stops mid-answer at 1:06:37; slides 2–4 and 84–104 are slide-file-only.

#### Images (Step 1c)
- [ ] raw/images/02-image-classification/ — select, render, embed in slide file and wiki (41 rendered, 5.0 MB, embedded in slide file; wiki pending)
- [x] Look at two rendered images against the slide-file claims (slide 99 squared-hinge curve agrees; slide 29's "narrow green spike into blue" was a broad wedge to the top edge, corrected)
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
