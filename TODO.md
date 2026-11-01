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
- [ ] raw/slides/01-introduction-part-1.md — number map, Sonnet transcription, --verify
- [ ] raw/slides/01-introduction-part-2.md — number map, Sonnet transcription, --verify
- [ ] Figure audit (Sonnet, 600 dpi crops) on chart/table/figure pages of both decks

### Transcript edit (Step 1a)
- [ ] raw/transcripts/01-introduction.md — Sonnet copy-edit; timestamp, number, ratio checks; proper-noun grep

### Images (Step 1c)
- [ ] raw/images/01-introduction-part-1/ — select, render, embed in slide file and wiki
- [ ] raw/images/01-introduction-part-2/ — select, render, embed in slide file and wiki
- [ ] Look at two rendered images against the slide-file claims
- [ ] INDEX.md image rules; AGENTS.md Images section + table rows; BUILD_LOG.md render record; LICENSE.md attribution

### Wiki
- [ ] wiki/01-introduction.md
- [ ] Topic pages (cross-lecture concepts introduced in lecture 1)
- [ ] INDEX.md table of contents

### Publish
- [ ] kb.json — coverage, materials.method, provenance caveats
- [ ] BUILD_LOG.md — lecture 1 record: notices, audit findings, printed slips, transcript edits
- [ ] SEE_ALSO.md, if a sibling KB is genuinely relevant
- [ ] verify_kb.py clean, and its review section read
- [ ] Commit and push
- [ ] PATCH kbUrl onto the catalog entry
- [ ] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work
