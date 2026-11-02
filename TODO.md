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
- [x] raw/slides/08-attention-transformers.md — Sonnet transcription (four agents, pages 1–31 / 32–62 / 63–92 / 93–122, all finished, chunks appended), --verify (122 headings; OK); header written by the parent; 25 quoted strings opening with math unquoted and 7 formulas rewritten for GitHub (check_math clean, 907 formulas)
- [x] Figure audit (Sonnet), two agents, 33 slides: 4, 20, 23, 24, 26, 27, 28, 38, 44, 47, 54, 55, 60, 61 and 63, 64, 65, 66, 81, 82, 87, 92, 93, 96, 98, 101, 105, 109, 110, 112, 113, 115, 121; 600 dpi crops (4 and 20 first from page views; 63 page view only). Corrections: 20 (s0 keeps its arrow into s1, an arrow drops into c1; the "+" feeds c2), 26 (purple cell block 5 by 4), 27 (gold column box takes three labels; a gold row-label box was omitted), 100–101 (no vertical line on the photo; patch contents). Additions: 81 (10 arrows), 93 and 112 (residual routing), 109 (arrow out of Pooling). Audit A's report contradicted itself on grid orientation; the text layer settled it (slides 43–61 key 1 at the top; the pasted figure on 4 and 121 at the bottom). Parent checked 19, 20, 27, 61 on 1400px renders
- [x] Worked arithmetic and drawn architectures recomputed / counted: slide 18 and 22 weights sum to 1; 104's 768; 115's 8D/3 (8D² both); blocks counted (2 on 4, 96–99, 105, 121; 3 on 92–95). Slips kept with [Ed:] lines: 62 (Y = AX, repeated faded on 63), 66 (√D_Q with D_Q undefined; repeated to 78), 77 (1.192 TB is 1,192 GiB at 2 bytes: mixed units; 1.28 TB decimal), 82 (O(N) memory, which 78 gives only with Flash Attention), 111 ("identify"), 113 (RMSNorm averages over N for a D-vector)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/08-attention-transformers.md — Sonnet copy-edit; 87/87 markers identical; ratios 0.75–0.96 after the parent moved "different word order … there's a little" back from 24:38 into 25:25 (the agent reported 0.68 as filler loss); 53:01 "blah blah blah" and "index 3" restored (paraphrased and respelled, unlisted); number diff otherwise all listed (10:01 "as zero" → s0 added to the header); capitalised words all in captions or slides; header corrected (23:05 slip sentence, the memory claim, the s0 → s1 arrow remark at 16:58 vs slides 17–19). 19 student-question markers, 1 partly audible; 6 [unclear]

#### Images (Step 1c)
- [x] raw/images/08-attention-transformers/ — rendered 23 (3 JPEG, 20 PNG; 3.1 MB): 5, 11, 19, 22, 23, 24, 27, 29, 35, 46, 47, 57, 59, 61, 66, 82, 91, 95, 99, 109, 111, 112, 120; embedded in the slide file (23); header lists every unrendered slide and why (99)
- [ ] Embed in the wiki page and topic pages; hand-written captions
- [x] Look at two rendered images against the slide-file claims (27 heatmap: gold and purple boxes as corrected; 61 diagram: −∞ and 0 cells, words) plus 19 (s0 → s1 arrow is drawn) and a scratch render of 20
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
