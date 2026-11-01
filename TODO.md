# KB build — CS231N

Open work only. Every run reads this file in full before doing anything and does
only unchecked work. Tick a box the moment its artifact is written, and commit
this file with it. When a run is committed and pushed, move its section verbatim
to [`BUILD_LOG.md`](BUILD_LOG.md): nothing ticked stays here.

## Run 1 — Lecture 1 (Introduction), 2026-11-01

Scope: lecture 1 only. Two decks (part 1 Fei-Fei Li, part 2 course overview).
Images opted in: every figure-bearing slide. PDFs link-only.

### Transcripts
- [x] 01 Introduction — video 2fq9wYslV0A (original captions in raw/transcripts/original/)

### Crawl
- [x] Fetch course site index: https://cs231n.stanford.edu/2025/
- [x] Download linked PDFs and slides (gitignored raw/pdfs/) — crawler treats /slides/2025/ as off-prefix (start is /2025/), so only lecture 1's two decks were fetched by hand into raw/pdfs/slides/; later runs fetch their own deck the same way. Handout links on schedule.html (handouts/*.pdf) 404 at the relative path.
- [x] Write sources.md

### Slides (Step 1b)
- [x] raw/slides/01-introduction-part-1.md — number map, Sonnet transcription, --verify (69 headings, 1:1; exit 0)
- [x] raw/slides/01-introduction-part-2.md — number map, Sonnet transcription, --verify (50 headings; printed 1–53, 4/5/45 absent; exit 0). Both decks print the number mid-footer after "Lecture 1 -"; slide_number_map.py missed it (corner/centre only) and was extended with a split-footer reading — 179 sibling decks unchanged by the patch.
- [x] Figure audit (Sonnet, 600 dpi crops) on chart/table/figure pages of both decks — part 1: 19, 29, 44, 48, 50, 62, 64, 66 → 6 clean; 62 one point mis-dated; 64 one wrong bar value (11,641 → 11,840.54), two values called illegible that read fine (23,886.79; 31,230.92), startup curve mis-dated. Part 2: 8, 14, 22, 34, 37, 43, 44, 52 → all clean (all 36 chart values on 34; grading sums to 100). Fixes applied.

### Transcript edit (Step 1a)
- [x] raw/transcripts/01-introduction.md — Sonnet copy-edit; timestamp, number, ratio checks; proper-noun grep. 81/81 markers identical; ratios 0.78–0.99; number diff = 3 deliberate ("2 and 1 halfd" → two-and-a-half-D; "assignment three" → Assignment 3; false start "22,000 images, oh sorry" dropped, "22,000 categories" kept). Names not on the slides (Roomba, Midjourney, Bell Labs, H&S) are all in the captions. 7 inline [unclear]/[Ed:] flags. Part 2 hand-over inside [44:25]; overview proper from [45:14].

### Images (Step 1c)
- [x] raw/images/01-introduction-part-1/ — select, render, embed in slide file and wiki (47 of 69)
- [x] raw/images/01-introduction-part-2/ — select, render, embed in slide file and wiki (17 of 50; 10.1 MB total with part 1)
- [x] Look at two rendered images against the slide-file claims (part 1 slide 63 chart, part 2 slide 17 diagram: both agree)
- [x] INDEX.md image rules; AGENTS.md Images section + table rows; BUILD_LOG.md render record; LICENSE.md attribution

### Wiki
- [x] wiki/01-introduction.md
- [x] Topic pages (cross-lecture concepts introduced in lecture 1): imagenet, computer-vision-tasks, course-logistics
- [x] INDEX.md table of contents

### Publish
- [x] kb.json — coverage, materials.method, provenance caveats
- [x] BUILD_LOG.md — lecture 1 record: notices, audit findings, printed slips, transcript edits
- [x] SEE_ALSO.md, if a sibling KB is genuinely relevant: MIT 6.7960, CS224N, CS224R
- [x] verify_kb.py clean, and its review section read (all hard checks pass incl. KaTeX + GitHub math; review: coverage 1/18 stated, part 2 gaps 4/5/45 deliberate, image counts and numeric claims match)
- [ ] Commit and push
- [ ] PATCH kbUrl onto the catalog entry
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
