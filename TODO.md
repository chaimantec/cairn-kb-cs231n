# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Open

- [ ] Lectures 5–18 — not started. Runs so far have covered lectures 1–4, at the user's request; add a
  run section (transcripts, decks from `https://cs231n.stanford.edu/slides/2025/lecture_N.pdf`,
  wiki, images if still wanted) when the user asks for more lectures. Video ids are in the
  catalog entry (`GET /api/catalog/5b4c7083-7bdd-4ca6-9e11-f8ed87717c71`).

## Run 4 — Lecture 4 (Neural Networks and Backpropagation), 2026-11-02

Scope: lecture 4 only, video 25zD5qJHYsk (76:47). One deck, `lecture_4.pdf`: 147 pages, printed
1–152, 2, 47 and 112–114 absent (hidden slides; footer spans either side of each gap in the same
position, sequence monotonic); page 55 prints no number (a figure credit sits there), labelled 57.
Ehsan Adeli per the schedule. Images opted in (every figure-bearing slide). PDFs link-only.
Slug `04-neural-networks-backpropagation`.

### Transcripts
- [x] 04 Neural Networks and Backpropagation — video 25zD5qJHYsk (original captions in raw/transcripts/original/; 99 paragraphs)

### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_4.pdf (title slide: "Lecture 4: Neural Networks and Backpropagation", April 10, 2025)
- [x] sources.md — the two handouts the schedule links by a broken relative path resolve at https://cs231n.stanford.edu/handouts/ (linear-backprop.pdf, derivatives.pdf: 200); record them

### Slides (Step 1b)
- [x] raw/slides/04-neural-networks-backpropagation.md — number map, Sonnet transcription (four agents, pages 1–37 / 38–74 / 75–111 / 112–147), --verify (147 headings; exit 0)
- [x] Figure audit (Sonnet), two agents: slides 10, 11, 19, 25, 26, 30, 33, 41, 42, 46, 50, 53 and 74, 96, 100, 104, 105, 116, 134, 136, 143, 148, 152. Both rendered below the 600 dpi asked for (150 and 200 dpi, with crops at 400–600 dpi on 11, 53 and 116). Errors on 11 (step levels 1.4 / 1.05 → 0.95 / 0.9, one label, arrows end above the curve), 25–26 (7 red and 15 blue points, not 8 and ~16; red column right of the θ axis), small omissions on 41, 96, 116, 134. Confirmed: no paths on 10; no figure on 50; plus sign printed in all three places on 53; every matrix entry on 143. Fixes applied.
- [x] Worked arithmetic recomputed: (x+y)z, the sigmoid graph (forward and every gradient), the gates, the ReLU vectors and slide 144's 256 GB all exact; slide 143's printed y = [[13, 9, -2, -6], [5, 2, 17, 1]] is not x·w = [[-1, -1, 2, 6], [5, 2, 11, 7]] (confirmed on the page by the audit and on the slide 150 render) — [Ed:] line; slide 53's plus sign — [Ed:] line

### Transcript edit (Step 1a)
- [x] raw/transcripts/04-neural-networks-backpropagation.md — Sonnet copy-edit; 99/99 markers identical; ratios 0.75–1.01; number diff: every difference traced (7:53 repeated "32" in "3264" dropped, 16:27 self-corrected "10 templates" dropped, 43:48 "x1" → x, 44:35 three → 3, 54:39 and 55:27 "x 2" → x squared, decimals at 56:12, 56:58, 57:44, 4,96 → 4096); parent fixes: 20:25 "their efficient models" (an insertion from the false start "for uh efficient") → "their models"; header said the hinge-loss digression had no slide (slide 6 prints it) and cited a nonexistent section map. Restored names all on the slides or in the captions (Swish, EfficientNet, polar, overfitting in the captions). 10 student-turn markers, 1 [unclear] (1:00:04). Recording skips slides 3–4 and 12–21; ends 1:16:19 at slides 151–152.

### Images (Step 1c)
- [x] raw/images/04-neural-networks-backpropagation/ — select, render (35; 5.2 MB; 31 JPEG, 4 PNG), embed in slide file (35)
- [x] Embed in the wiki page (35, all with hand-written captions) and topic pages (neural-networks 9, backpropagation 13, regularization 1, gradient-descent 1); four blocks moved by hand (33, 42, 104 on the backpropagation page, 105)
- [x] Look at two rendered images against the slide-file claims (slide 150: every matrix entry as transcribed, so slide 143's slip is real; slide 26: 7 red and 15 blue in both panels, as the audit found)
- [x] INDEX.md image rules; AGENTS.md table row (and three general lessons: audit agents under-render; credit lines dropped by transcribers; the colon rule covers tables and code); BUILD_LOG.md render record; LICENSE.md attribution

### Wiki
- [x] wiki/04-neural-networks-backpropagation.md (slips on slides 53 and 143 noted; slides 3–4 and 12–21 marked slide-only)
- [x] Topic pages: neural-networks, backpropagation; links from gradient-descent, linear-classifiers, regularization (new section on λ vs. network size), loss-functions, hyperparameters-and-validation, learning-rate-schedules, the 01, 02 and 03 pages, and the course-logistics roadmap (row 4; its stale "only lecture 1" sentence fixed)
- [x] INDEX.md table of contents (coverage 4 of 18; lecture 4 citation rule; skipped slides; printed-slips rule)

### Publish
- [x] kb.json — coverage (4 of 18; 14 topic pages), decks 5/5, figure audit 5/5 (with lecture 4's low-dpi note), images 164 (byLecture 4: 35; 146 JPEG, 18 PNG), caveats for lecture 4 coverage, numbering and slips
- [x] BUILD_LOG.md — lecture 4 record
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
