# Build log — CS231N knowledge base

The record of how this knowledge base was built and checked, one section per
finished run, in order: each deck's licence notices and lecture pointers, each
transcript's edit and checks, what each figure audit found, each deck's printed
slips, and which slides were rendered as images and why the others were not.
A run's section is its `TODO.md` checklist, moved here verbatim once the run
was committed and pushed. It holds no unchecked box: open work lives only in
`TODO.md`.

It is a build record, **not needed to answer questions**: every fact a learner
needs is on the wiki page, slide file or transcript it concerns. The rules
every build follows, and each lesson in general form, are in
[`AGENTS.md`](AGENTS.md).

## Index

| Lecture | Runs |
| --- | --- |
| 1 Introduction | [Run 1](#run-1--lecture-1-introduction-2026-11-01) |
| 2 Image Classification with Linear Classifiers | [Run 2](#run-2--lecture-2-image-classification-with-linear-classifiers-2026-11-02) |
| 3 Regularization and Optimization | [Run 3](#run-3--lecture-3-regularization-and-optimization-2026-11-02) |
| 4 Neural Networks and Backpropagation | [Run 4](#run-4--lecture-4-neural-networks-and-backpropagation-2026-11-02) |
| 5 Image Classification with CNNs | [Run 5](#run-5--lecture-5-image-classification-with-cnns-2026-11-02) |
| 6 Training CNNs and CNN Architectures | [Run 6](#run-6--lecture-6-training-cnns-and-cnn-architectures-2026-11-02) |
| 7 Recurrent Neural Networks | [Run 7](#run-7--lecture-7-recurrent-neural-networks-2026-11-02) |

## Runs

_Each finished run's section is appended below._

## Run 1 — Lecture 1 (Introduction), 2026-11-01

Scaffolded the repo and built lecture 1 end to end: transcript, both decks, figure audits,
transcript edit, wiki page, three topic pages (ImageNet, computer vision tasks, course
logistics), 64 slide images, INDEX, SEE_ALSO, kb.json. Images were opted in by the user; PDFs are
link-only; the verbatim captions are gitignored (as in CS224R and CS336).

### Lecture 1 record

**Decks.** Two: `lecture_1_part_1.pdf` (69 pages, Fei-Fei Li's history; printed numbers equal
PDF pages) and `lecture_1_part_2.pdf` (50 pages, Ehsan Adeli's overview; printed 1–53 with 4, 5
and 45 absent — page 4 = slide 6, page 43 = slide 46). Both print the number as a separate span
after "Lecture 1 -" in the footer; part 1 pages 15 and 61 print it bare in the bottom-right
corner. Neither deck nor the course site states a licence; per-image credit lines are printed
on 14 slides of part 1 and 10 of part 2, three of them "Figures copyright … Reproduced with
permission" (part 1, slides 49, 50, 54, 57).

**Figure audit** (Sonnet, 600 dpi crops, eight slides per deck). Part 1: 19, 29, 44, 48, 50, 62,
64, 66 — six agreed. Slide 62 had one GPU point dated mid-2018 that sits on the Jan-19 gridline.
Slide 64 had one wrong bar value (11,641 for 11,840.54), called the last two bar values
illegible when they read 23,886.79 and 31,230.92, and placed several points of the startups curve
at the wrong years. All corrected. Part 2: 8, 14, 22, 34, 37, 43, 44, 52 — all agreed, including
all 36 values of the CVPR statistics chart and the grading weights (sum 100%, plus up to 3% extra
credit). Parent check of two renders (part 1 slide 63 chart, part 2 slide 17 diagram) also
agreed. The parent removed two transcriber inferences that the audit did not flag: slide 44's
untitled axis called "top-5 error", and slide 43's five output labels called "top-5 predictions"
with the underlined one "correct".

**Printed slips, transcribed as printed.** Part 1: slide 14 "530-540million"; slide 23
"Elshlager" (Elschlager); slide 39 title 1986 but timeline box "1985 Backprop"; slide 41's
timeline drops "Caltech101" ("2007 PASCAL") which slides 35 and 43–49 print; slide 48 legend
truncated ("Subm…", "Acce…"); slide 50 "ffordshire bullterrier"; slide 51 "Fabaret et al, 2012"
(Farabet); slide 58 is a black rectangle where an embedded video did not render. Part 2: slide 51
names the third and fourth parts differently from the agenda slides 6–30; slide 50's last line is
clipped by the footer. Talk versus slide: Li gives human ImageNet error as "under, say, 3%"
(≈33:35); slide 44 prints 5.1.

**Transcript edit** (Sonnet). 81 paragraphs; marker sequence identical; word ratios 0.78–0.99;
about 65 restorations listed in the header. Number diff: three deliberate changes ("2 and 1
halfd" → two-and-a-half-D; "assignment three" → Assignment 3; the false start "22,000 images, oh
sorry" dropped with "22,000 categories" kept). Seven inline flags: [14:54] "linker" → nature
(Ed) and an inferred `*[Student answer, inaudible]*`; [30:27] "quasi-solved" unclear; [40:30]
"Juan building" → Huang Building (Ed; slide 40 says "Huang Basement"); [41:18] "by any measure"
unclear; [42:52] "HNS" → H&S unclear; [1:00:14] "Antonio" → Yoshua (Ed; part 2, slide 31).
Restored names not on any slide (Roomba, Midjourney, Bell Labs, H&S) are all present in the raw
captions. The hand-over to Adeli is inside [44:25]; his overview proper starts at [45:14]. The
recording skips part 2, slides 33–48 and 50.

**Images.** 64 rendered (60 JPEG, 4 PNG; 10.1 MB): part 1 — 8, 12, 14–17, 19–24, 27, 29, 30,
32–41, 43, 44, 46–57, 59, 61–64, 66–68; part 2 — 8–10, 14–18, 22–28, 34, 52. Not rendered, part 1:
1 (title), 2–4 (anniversary collage, staff photographs), 5–7 and 9–11 (intermediate Venn builds),
13, 18, 26, 65, 69 (agenda/dividers), 25 (text), 28 (plain grey fixation frame), 31 (recap of 27,
29, 30), 42 (41 plus one line), 45 (44 plus an arrow), 58 (black rectangle), 60 (same layout as
59). Part 2: 1 (title), 2–3 (staff and guest-lecturer photos), 6, 11–13, 19–21, 29, 30, 35 (agenda,
dividers, title-only), 7 (subset of 8), 31–33 (award-winner and ceremony photographs), 37 (schedule
screenshot; table transcribed), 36, 38–44, 46–51, 53 (text). The raster test flagged all 69 part 1
pages until a template image on every page was excluded (then 53), and missed the vector Venn
diagram and GFLOP charts; the slide-file prose decided. All 64 images are cited by the lecture
page; the topic pages carry 7 (imagenet), 10 (computer-vision-tasks) and 1 (course-logistics).
Thirteen captions are hand-written (part 1: 8, 19, 22, 29, 37, 44, 47, 63, 66; part 2: 14, 17, 22,
25). The longest stretch with no figure is 14:08–17:16 (3D as an ill-posed problem; vision versus
language), which the wiki carries in prose and marks as transcript-only.

**Skill scripts changed in this run** (in the `cairn-kb` skill, not this repo):
`slide_number_map.py` gained a split-footer reading (a bare number whose left neighbour on the
same line ends in a separator), filled from the corner reading on pages without a footer; all
179 sibling decks on disk map identically before and after. `embed_slide_images.py` gained
`--deck-label` for lectures with several decks. `verify_kb.py` now sums image directories and
slide files per lecture (so `byLecture`, `lecturesWithImages` and the AGENTS.md table count a
two-deck lecture once).

### Run 1 checklist (moved verbatim from TODO.md)

Scope: lecture 1 only. Two decks (part 1 Fei-Fei Li, part 2 course overview).
Images opted in: every figure-bearing slide. PDFs link-only.

#### Transcripts
- [x] 01 Introduction — video 2fq9wYslV0A (original captions in raw/transcripts/original/)

#### Crawl
- [x] Fetch course site index: https://cs231n.stanford.edu/2025/
- [x] Download linked PDFs and slides (gitignored raw/pdfs/) — crawler treats /slides/2025/ as off-prefix (start is /2025/), so only lecture 1's two decks were fetched by hand into raw/pdfs/slides/; later runs fetch their own deck the same way. Handout links on schedule.html (handouts/*.pdf) 404 at the relative path.
- [x] Write sources.md

#### Slides (Step 1b)
- [x] raw/slides/01-introduction-part-1.md — number map, Sonnet transcription, --verify (69 headings, 1:1; exit 0)
- [x] raw/slides/01-introduction-part-2.md — number map, Sonnet transcription, --verify (50 headings; printed 1–53, 4/5/45 absent; exit 0). Both decks print the number mid-footer after "Lecture 1 -"; slide_number_map.py missed it (corner/centre only) and was extended with a split-footer reading — 179 sibling decks unchanged by the patch.
- [x] Figure audit (Sonnet, 600 dpi crops) on chart/table/figure pages of both decks — part 1: 19, 29, 44, 48, 50, 62, 64, 66 → 6 clean; 62 one point mis-dated; 64 one wrong bar value (11,641 → 11,840.54), two values called illegible that read fine (23,886.79; 31,230.92), startup curve mis-dated. Part 2: 8, 14, 22, 34, 37, 43, 44, 52 → all clean (all 36 chart values on 34; grading sums to 100). Fixes applied.

#### Transcript edit (Step 1a)
- [x] raw/transcripts/01-introduction.md — Sonnet copy-edit; timestamp, number, ratio checks; proper-noun grep. 81/81 markers identical; ratios 0.78–0.99; number diff = 3 deliberate ("2 and 1 halfd" → two-and-a-half-D; "assignment three" → Assignment 3; false start "22,000 images, oh sorry" dropped, "22,000 categories" kept). Names not on the slides (Roomba, Midjourney, Bell Labs, H&S) are all in the captions. 7 inline [unclear]/[Ed:] flags. Part 2 hand-over inside [44:25]; overview proper from [45:14].

#### Images (Step 1c)
- [x] raw/images/01-introduction-part-1/ — select, render, embed in slide file and wiki (47 of 69)
- [x] raw/images/01-introduction-part-2/ — select, render, embed in slide file and wiki (17 of 50; 10.1 MB total with part 1)
- [x] Look at two rendered images against the slide-file claims (part 1 slide 63 chart, part 2 slide 17 diagram: both agree)
- [x] INDEX.md image rules; AGENTS.md Images section + table rows; BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [x] wiki/01-introduction.md
- [x] Topic pages (cross-lecture concepts introduced in lecture 1): imagenet, computer-vision-tasks, course-logistics
- [x] INDEX.md table of contents

#### Publish
- [x] kb.json — coverage, materials.method, provenance caveats
- [x] BUILD_LOG.md — lecture 1 record: notices, audit findings, printed slips, transcript edits
- [x] SEE_ALSO.md, if a sibling KB is genuinely relevant: MIT 6.7960, CS224N, CS224R
- [x] verify_kb.py clean, and its review section read (all hard checks pass incl. KaTeX + GitHub math; review: coverage 1/18 stated, part 2 gaps 4/5/45 deliberate, image counts and numeric claims match)
- [x] Commit and push — https://github.com/chaimantec/cairn-kb-cs231n (public; INDEX.md and images fetch 200 from raw.githubusercontent.com)
- [x] PATCH kbUrl onto the catalog entry — re-fetched: kbUrl = https://github.com/chaimantec/cairn-kb-cs231n
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 2 — Lecture 2 (Image Classification with Linear Classifiers), 2026-11-02

Built lecture 2 end to end: transcript, the deck, a figure audit, the transcript edit, the wiki
page, five topic pages (image classification, k-nearest neighbours, hyperparameters and
validation, linear classifiers, loss functions), 41 slide images, and updates to INDEX, AGENTS,
LICENSE, kb.json, course logistics, computer vision tasks and the lecture 1 page. Images were
opted in again; PDFs stay link-only.

### Lecture 2 record

**Deck.** One: `lecture_2.pdf`, 102 pages, Ehsan Adeli (per the course schedule; the recording
does not name him), April 3, 2025. Printed numbers 1–104 with 32 and 49 absent: page 32 = slide 33,
page 48 = slide 50. Footer "Lecture 2 - N" as a separate span. On page 32 the "33" box starts
inside the "Lecture 2 -" box (x0 496 against x1 499), so `slide_number_map.py`'s split-footer test
missed it and its corner fallback read a "1" subscript from the page's equations as the slide
number. Fixed in the script (the left neighbour must start left of the number and end before its
midpoint); all 541 decks on disk re-mapped identically apart from that page. No deck-wide licence
statement; per-image credit lines on 18 slides (CC-BY 2.0, CC0, public domain, Canny 1986,
Krizhevsky 2009, Wolfram Cloud, a LinkedIn image source).

**Transcription.** Three Sonnet agents in parallel (pages 1–34, 35–68, 69–102), about 75k tokens
each; the parent assembled the file, wrote the front matter and section table, and fixed two math
renders (`\\` in a cases block → `\cr`; a `$|$` image-pair notation rewritten in prose).
`--verify` clean.

**Figure audit** (Sonnet, 600 dpi crops, 14 slides: 8, 23, 30, 33, 45, 57, 60, 62, 63, 64, 65, 74,
94, 101). Eight agreed. Slide 8: the pixel array called "tiny, not transcribed, about 20 × 15" was
legible at 600 dpi and is 24 × 16; the first row and value range are now given. Slide 33: the L1
path from O to B goes up the axis first, then right, not the reverse. Slide 64: the third blue
circle is left of the vertical axis, not right. Slide 30's white tie regions and slide 63's
image placement were loosely described and are now exact. Slide 45's means were only roughly
given; the audit's per-k reading (dots, mean, error bar) is now a table. The parent's own check of
two renders: slide 99's squared-hinge curve agreed; slide 29's "narrow green spike into blue" was a
broad green wedge to the top edge, corrected.

**Printed slips, transcribed as printed.** Slide 3 has a sentence missing its verb ("your assigned
TA for initial guidance"); slide 24's code uses Python 2 `xrange`; slide 33 prints
"d2(O,A) = d2(O,A) = 1" (second should be O,B); slide 45 "bars indicated standard deviation";
slide 69 "is a average"; slide 74 prints the frog probability as 0.00 (0.18/188.7 ≈ 0.001);
slide 80 prints "H(p)" with a lowercase p; slides 81 and 102 print the exponent as "s y_i" without
the subscript; slide 100's comment reads "only sum j is not y_i". Two are arithmetic slips the
parent found by recomputing every worked example: slide 60's ship score 61.95 omits the bias
(60.75 with it), and slide 101's −log(0.353) = 0.452 is base 10 (natural log ≈ 1.04, as slides
76 and 83 use). Both carry an `[Ed:]` line in the slide file and a note on the wiki page. All
other worked values recompute exactly (slide 23's 456; slides 73–76; slides 91–94's 2.9, 0, 12.9
and 5.27; slide 101's scores and hinge loss 1.58).

**Transcript edit** (Sonnet, ~100k tokens). 87 paragraphs; marker sequence identical; word ratios
0.74–1.00; 26 restorations in the header. Number diff: 01 → O(1); "20 five minutes" →
`[Ed: 25 minutes]`; "372" → `[Ed: 3072]` three times (slides 52–55); "2x two" → 2x2; "C4" →
CIFAR-10; "CS2 229" → CS 229. One unlisted "2" traced to [34:51], where the editor had turned
"while there we have" into "while with L2 we have"; reverted. Restored terms all appear in the
deck, except "GPT", which is in the captions ("that GPT"). Five inline flags: [42:39] accuracy
"29 28%"; [46:29] 25 minutes; [48:01] 3072 ×3; [1:01:13] "the value of 3"; [1:06:37] captions end
mid-sentence. Student-turn markers at [7:01] (two), [20:56], [21:42], [24:01], [32:32], [38:00],
[44:58], [1:05:04] (two); the editor's header also listed [1:05:51], which has none, corrected.
**Coverage:** the recording starts at slide 5 (slides 2–4 unspoken) and ends at 1:06:37 during
slide 83's second question; slides 84–104 (coming up, SVM reading assignment, softmax vs. SVM)
are slide-only. The deck's backup slides, mentioned at [2:24], are not in the posted PDF.

**Images.** 41 rendered (38 JPEG, 3 PNG; 5.0 MB): 7–16, 18, 19, 22, 23, 29–31, 33–35, 41, 42, 44, 45,
47, 48, 55–57, 60, 62–65, 77, 80, 84, 89, 94, 99, 101. Not rendered: 1 (title); 2–6
(administrative, syllabus, agenda); 17, 21, 24–28, 100 (code); 20, 51, 70 (section titles); 36,
50, 85 (text); build steps whose final step is rendered (37–40 → 41, 43 → 44, 46 → 47, 52–54 → 55,
59 → 60, 61 → 62, 71–76 → 77, 78–79 → 80, 86–88 → 89, 90–93 → 94, 95–98 → 99); 58 (CIFAR-10 grid
repeated from 44); 66–69 (score table transcribed in full); 81–83, 102–104 (formulas and questions
transcribed exactly). The raster test flagged 76 of 102 pages (no recurring template image this
time); the slide-file prose and the agents' per-slide figure tables decided. All 41 are cited by
the lecture page; the topic pages carry 4 (image-classification), 6 (k-nearest-neighbors), 3
(hyperparameters-and-validation), 7 (linear-classifiers) and 7 (loss-functions), embedded with
`--deck-label "Lecture 2"`. Sixteen captions are hand-written (8, 15, 23, 30, 33, 34, 45, 47, 48,
60, 62, 63, 64, 80, 89, 101) and reused on the topic pages. The embed script first anchored slide
101 on the introduction's "slides 101–104"; the range was reworded and the image re-placed.

### Run 2 checklist (moved verbatim from TODO.md)

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
- [x] raw/images/02-image-classification/ — select, render, embed in slide file and wiki (41 rendered, 5.0 MB; all 41 in the lecture page; 27 on topic pages via --deck-label "Lecture 2"; 16 hand-written captions)
- [x] Look at two rendered images against the slide-file claims (slide 99 squared-hinge curve agrees; slide 29's "narrow green spike into blue" was a broad wedge to the top edge, corrected)
- [x] INDEX.md image rules; AGENTS.md table row; BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [x] wiki/02-image-classification.md (slide 60 and 101 arithmetic slips noted; SVM and softmax-vs-SVM sections marked slide-only)
- [x] Topic pages (cross-lecture concepts introduced in lecture 2): image-classification, k-nearest-neighbors, hyperparameters-and-validation, linear-classifiers, loss-functions; links added from computer-vision-tasks, course-logistics (lecture 2 announcements) and 01-introduction
- [x] INDEX.md table of contents (coverage 2 of 18; citation rules for lecture 2; slide-only sections)

#### Publish
- [x] kb.json — coverage, images, caveats
- [x] BUILD_LOG.md — lecture 2 record
- [x] verify_kb.py clean, and its review section read (exit 0; chat KaTeX and github.com MathJax both clean after fixing one inline H(p) formula that GitHub left as raw text and two display-math blocks set mid-sentence; numeric claims in INDEX/AGENTS match the image table)
- [x] Commit and push — af4c210 on https://github.com/chaimantec/cairn-kb-cs231n (INDEX, lecture page, topic pages and images fetch 200 from raw.githubusercontent.com); kbUrl already set on the catalog entry since run 1
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 3 — Lecture 3 (Regularization and Optimization), 2026-11-02

Built lecture 3 end to end: transcript, the deck, a figure audit, the transcript edit, the wiki
page, four topic pages (regularization, gradient descent and SGD, optimizers, learning-rate
schedules), 24 slide images, and updates to INDEX, AGENTS, LICENSE, kb.json, the course-logistics
roadmap, linear classifiers, loss functions, hyperparameters and validation, and the lecture 2
page. Images were opted in again; PDFs stay link-only.

### Lecture 3 record

**Deck.** One: `lecture_3.pdf`, 119 pages, Zane Durante (per the course schedule; the recording
does not name him), April 8, 2025. Printed numbers 1–123 with 10, 11, 12 and 29 absent: page 10 =
slide 13, page 26 = slide 30. Footer "Lecture 3 - N" as a separate span. Every page read a printed
number from the same footer position and the sequence only increases; the raw spans on pages 9–10
(9 → 13) and 25–26 (28 → 30) confirm both gaps are hidden slides, not misreads. Slides 102–123
are an appendix titled "Slides from Previous Years". No deck-wide licence statement; per-image
credit lines on slides 6, 7 (CC-BY 2.0 Nikita, Umberto Salvagnin, jonsson; CC0), 31, 32 (CC0), 46
(public domain), 59 (Wikipedia "Saddle_point") and 80 (a fast.ai post). The schedule lists the
course notes "Optimization" (cs231n.github.io/optimization-1/) as the reading.

**Transcription.** Three Sonnet agents in parallel (pages 1–40, 41–80, 81–119), about 83k tokens
each. The first stopped at slide 40, having written 36 of its 40 headings, and gave slides 41–44
only as summaries in its report; it was resumed by message to append them in full. The parent
assembled the file, wrote the front matter and section table, and fixed 15 GitHub italics
warnings (`}_` and `)_` in math) and four inline formulas set straight after a quotation mark.
`--verify` clean (119 headings).

**Figure audit** (Sonnet, 600 dpi crops, 19 slides: 13, 18, 27, 34, 41, 55, 57, 61, 70, 75, 80,
83, 84, 86, 89, 99, 109, 119, 122). Slide 80: wd and L2 values wrong at epochs 6 and 15 (L2's dip
to 0.813 at epoch 15 was missed; L2 is above wd at epochs 2 and 6); replaced with the audit's
per-epoch readings. Slide 84: the plateaus are about 1.4 (not 1.3) and 1.1 (not 1.0). Slide 99:
the red points sit just right of the θ axis, not left, and there are 15 blue points, not 17.
Small omissions: bold correct-class scores on slides 13 and 122; slide 86 reaches zero loss at
about epoch 250–260, not 260–270. Slides 61 (gradient-noise panel), 70, 75 and 109 confirmed to
carry no optimizer paths, only the heat-map and a vector legend: animation frames. Every number on
slides 34, 41, 119 and 122 checked cell by cell and exact. The parent's own check of two renders
outside the sample: slide 88's inverse-sqrt curve and slide 104's momentum and Nesterov diagram
both agree with the file.

**Printed slips, transcribed as printed.** Slide 119 repeats lecture 2's slide 101 and its
base-10 −log(0.353) = 0.452 (natural log about 1.04); `[Ed:]` line and wiki note. Slide 34's code
returns 0.1555 and the slide says "15.5%", a truncation; `[Ed:]` line. Slide 33's code is Python 2
(`xrange`, `print` statement) and says "tructated"; slides 71 and 73–80 print an extra closing
parenthesis at the end of the Adam update; slide 85 "Child at al"; slide 116 "BGFS" (BFGS on the
next line); slide 121 "2W is also has L = 0"; slide 91 "Use gradient form linear approximation";
slide 13 "is a average". Recomputed and exact: the numeric gradients −2.5, 0.6 and 0 (slides 39,
41, 43); slide 119's scores, exponentials, probabilities and hinge loss 1.58; slide 122's 2.9 and 0
and both of its hinge columns; slide 108's rearranged Nesterov update; the L2 penalties 1 and 0.25
of slides 24–25.

**Transcript edit** (Sonnet, ~100k tokens). 90 paragraphs; marker sequence identical; word ratios
0.80–0.97; 19 restoration rows in the header. Number diff: the only additions were "beta one, beta
two" → beta1, beta2 at [53:48] and [54:35], listed; nothing lost. Restored terms all appear in the
deck or the captions ("llama" is in the captions at [57:41]); Nesterov, AdaGrad and L-BFGS appear
only in the header's coverage note. Three inline flags: [28:35], [41:34], [1:06:09] ("best by
test"). 26 student-turn markers at [8:34] (two), [12:29] (two), [17:06], [20:10], [20:57],
[21:43], [22:29], [31:37], [33:09] (five), [35:27], [38:31], [40:48], [46:12], [46:58], [47:43],
[48:30], [52:17] (two), [55:22], [58:27]; the body matches the header's list. [20:57]'s question
may be the lecturer's own. **Coverage:** the recording starts at the recap (slide 5) and ends at
1:08:25 in slides 96–99; slides 2–4, 100–101 and 102–123 are slide-only. The L1/L2 distance
diagram discussed at ≈3:57–4:42 is not in the posted deck.

**Images.** 24 rendered (17 JPEG, 7 PNG; 2.8 MB): 18, 28, 35, 46, 50, 51, 55, 57, 59, 61, 80,
83–89, 91, 92, 99, 104, 119, 122. Not rendered: 1 (title); 2–4 (administrative); 5, 30, 102
(dividers); 6–9 (recaps of lecture 2 figures); 13–15, 19–26, 33, 34, 36–45, 47, 49, 52, 62–69,
71–74, 76–79, 81, 93, 94, 96, 97, 100, 105–108, 110, 115–117, 120, 121, 123 (tables, formulas,
vectors and code transcribed exactly); 48, 95, 101, 118 (text); build steps whose last step is
rendered (16–17 → 18, 27 → 28, 31–32 → 35, 53–54 → 55, 56 and 58 → 57, 82 → 83, 90 → 91 and 92,
98 → 99, 103 → 104); 60, 70, 75, 109 (animation frames with no paths); 111–114 (AdaGrad slides
repeating slide 53's contour plot). The raster test flagged 81 of 119 pages, with no recurring
template image; most of the gap to 24 is code listings and equations pasted as images. All 24 are
in the lecture page with 20 hand-written captions; the topic pages carry 2 (regularization), 7
(gradient-descent), 3 (optimizers) and 7 (learning-rate-schedules), embedded with
`--deck-label "Lecture 3"` and the same captions. Three embed problems, all fixed by hand: the
script expands a range under 12 slides to every member, so the intro's "slides 96–99" would have
pulled slide 99's image into it (reworded); paragraphs ending "(slide N):" got the image between
the sentence and its formula (slides 35 and 85 on the lecture page, 85 and 104 on the topic
pages); and the parent's first drafts placed images by hand, which were stripped and re-embedded
with the script.

**Wiki.** Lecture page with recording coverage, the missing animations, administrative notes
(slides only), the recap, regularization, optimisation, SGD's problems, momentum, RMSProp, Adam,
AdamW, learning-rate schedules, second-order methods, practice, the look ahead, and the
slide-only appendix. Four topic pages. Existing pages updated: linear-classifiers and
loss-functions no longer say lecture 3 is uncovered; hyperparameters-and-validation gains λ, the
learning rate and Adam's betas; the lecture 2 page links forward; the course-logistics roadmap
links lectures 2 and 3 (lecture 2's row had never been linked).

### Run 3 checklist (moved verbatim from TODO.md)

Scope: lecture 3 only, video dyNGd06MWn4 (68:39). One deck, `lecture_3.pdf`: 119 pages, printed
1–123, 10–12 and 29 absent (hidden slides; raw footer spans confirm, every page reads a printed
number, sequence monotonic). Images opted in (every figure-bearing slide). PDFs link-only.
Slug `03-regularization-optimization`.

#### Transcripts
- [x] 03 Regularization and Optimization — video dyNGd06MWn4 (original captions in raw/transcripts/original/)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_3.pdf (title slide: "Lecture 3: Regularization and Optimization", April 8, 2025)

#### Slides (Step 1b)
- [x] raw/slides/03-regularization-optimization.md — number map, Sonnet transcription (three agents, pages 1–40 / 41–80 / 81–119; the first stopped at slide 40 and was resumed to append 41–44), --verify (119 headings; exit 0); 15 GitHub italics warnings fixed
- [x] Figure audit (Sonnet, 600 dpi crops) on 19 slides: 13, 18, 27, 34, 41, 55, 57, 61, 70, 75, 80, 83, 84, 86, 89, 99, 109, 119, 122 → errors on 80 (wd and L2 values at epochs 6 and 15; L2 above wd at 2 and 6), 84 (plateau levels 1.4 and 1.1, not 1.3 and 1.0), 99 (red points right of the θ axis, not left; 15 blue points, not 17); small omissions on 13 and 122 (bold correct-class scores) and 86 (zero loss at 250–260); trajectory-free heat-maps on 61, 70, 75, 109 confirmed. Fixes applied.

#### Transcript edit (Step 1a)
- [x] raw/transcripts/03-regularization-optimization.md — Sonnet copy-edit; 90/90 markers identical; ratios 0.80–0.97; number diff: only "beta one, beta two" → beta1, beta2 (listed); no number lost. Restored terms all on the slides or in the captions ("llama" at [57:41]); Nesterov, AdaGrad, L-BFGS appear only in the header's coverage note. 26 student-turn markers and 3 [unclear] flags, all matching the header. Recording covers slides 5–99 and ends at 1:08:25; slides 2–4 and 100–123 are slide-file-only.

#### Images (Step 1c)
- [x] raw/images/03-regularization-optimization/ — select, render, embed in slide file and wiki (24 rendered, 2.8 MB, 17 JPEG + 7 PNG; all 24 in the lecture page; 19 on topic pages)
- [x] Look at two rendered images against the slide-file claims (slide 88 inverse-sqrt curve and slide 104 momentum vs. Nesterov diagram, neither in the audit sample: both agree)
- [x] INDEX.md image rules; AGENTS.md table row (and two general lessons: animation frames; range expansion and colon-before-formula in the embed script); BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [x] wiki/03-regularization-optimization.md (24 images via the embed script, 20 hand-written captions; slide 34 truncation, slide 119 base-10 log noted; appendix and slides 100–101 marked slide-only; trajectory-free animation slides explained)
- [x] Topic pages (cross-lecture concepts introduced in lecture 3): regularization, gradient-descent, optimizers, learning-rate-schedules (19 images via --deck-label "Lecture 3", captions reused); links from linear-classifiers, loss-functions, hyperparameters-and-validation, 02-image-classification and the course-logistics roadmap (rows 2 and 3 now linked)
- [x] INDEX.md table of contents (coverage 3 of 18; lecture 3 citation rule; slide-only appendix; missing animations)

#### Publish
- [x] kb.json — coverage (3 of 18; 12 topic pages), decks 4/4, figure audit 4/4, images 129 (byLecture 3: 24; 115 JPEG, 14 PNG), caveats for lecture 3 coverage, animations, slips
- [x] BUILD_LOG.md — lecture 3 record
- [x] verify_kb.py clean, and its review section read (exit 0; one inline formula GitHub left as raw text, "(O(n^3))" in parentheses, rephrased; image and page counts in INDEX/AGENTS match the measured table; AGENTS range-expansion sentence corrected to "up to 12 slides")
- [x] Commit and push — a6b5fb5, 915a917, 747b7a3 on https://github.com/chaimantec/cairn-kb-cs231n (INDEX, lecture page, topic pages, slide file, transcript, images and kb.json fetch 200 from raw.githubusercontent.com); kbUrl already set on the catalog entry since run 1
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 4 — Lecture 4 (Neural Networks and Backpropagation), 2026-11-02

Built lecture 4 end to end: transcript, the deck, two figure audits, the transcript edit, the wiki
page, two topic pages (neural networks; backpropagation and computational graphs), 35 slide
images, and updates to INDEX, AGENTS, LICENSE, kb.json, sources.md, the course-logistics roadmap
(row 4 linked; its "only lecture 1" sentence, stale since run 2, corrected), regularization,
gradient descent, loss functions, linear classifiers, hyperparameters and validation, learning-rate
schedules, and the lecture 1, 2 and 3 pages. Images opted in again; PDFs stay link-only.

### Lecture 4 record

**Deck.** One: `lecture_4.pdf`, 147 pages, Ehsan Adeli (per the course schedule; the recording
does not name the lecturer), April 10, 2025. Printed numbers 1–152 with 2, 47, 112, 113 and 114
absent: page 2 = slide 3, page 46 = slide 48, page 110 = slide 115. Footer "Lecture 4 - N" as a
separate span at x≈494; the spans either side of every gap sit in the same position and the
sequence only increases. Page 55 prints no number (a Karpathy figure credit sits where it would be)
and is labelled 57, the only number between 56 and 58. On page 18 (slide 19) a full-page Sora
frame is drawn over the title, footer and link, which remain in the text layer, so the map reads
the number and the page shows none. No deck-wide licence. Per-image credits: slide 7 (CC0 1.0
landscape and walking man), 13 (Sam Altman / OpenAI), 14 (Ramesh et al. 2022), 15–16 (Betker et
al. 2023), 17 (OpenAI GPT-4; "Source: Barnorama" inside the screenshot), 18 (Kirillov et al.
2023), 19–21 (OpenAI Sora link), 43 (Fotis Bobolas, CC-BY 2.0), 44–46 (Felipe Perucho, CC-BY
3.0), 48–49 (CC0; Xie et al. ICCV 2019), 50 (London and Hausser), 55 (Krizhevsky, Sutskever and
Hinton 2012, "Reproduced with permission"), 56–57 (Karpathy, "reproduced with permission").
Schedule readings: the Backprop course notes, the linear-backprop and derivatives handouts,
Efficient BackProp (LeCun et al.), and Why Momentum Really Works; the two handouts resolve at
`https://cs231n.stanford.edu/handouts/`, not under `/2025/` where the schedule's relative link
points, and are now in `sources.md`.

**Transcription.** Four Sonnet agents in parallel (pages 1–37, 38–74, 75–111, 112–147), 78–84k
tokens each, all finished, every chunk appended as written. `--verify` clean (147 headings). The
parent removed one inference (slide 116: "each operator in PyTorch is implemented as its own
file", not printed), restored slide 18's citation "Kirillov et al., Segment Anything, 2023" (found
by grepping the text layer's credit lines against the file), rewrote slide 19's heading, and fixed
19 GitHub math warnings (`\\` and `\,` in math, `)_` before subscripts, inline math after a quote
mark, math inside the italic `[Ed:]` lines).

**Figure audit** (Sonnet, two agents, 23 slides). A: 10, 11, 19, 25, 26, 30, 33, 41, 42, 46, 50,
53. B: 74, 96, 100, 104, 105, 116, 134, 136, 143, 148, 152. Both rendered below the 600 dpi asked
for: A at 150 dpi with `pdftoppm` (it reported PyMuPDF missing in its environment), cropping to
400–600 dpi only for 11 and 53; B at 200 dpi, with 600 and 900 dpi for 116. Errors: slide 11's
step levels (about 1.4 after epoch 30, 1.05 falling to 0.95 after 60, 0.9 after 90, not 1.5 and
1.3; one "Reduce learning rate" label; arrows end above the curve); slides 25–26 have 7 red and 15
blue points, not 8 and about 16, and the red column sits right of the θ axis. Omissions: 41 (an
upper-left green region in the 3- and 6-neuron panels), 96 (the derivative table, every other
gradient, the rectangle around w0 and x0), 116 (the last rows' commit messages), 134 (the second
set of arrows). Confirmed: no optimizer paths on 10 (an animation frame); no figure at all on 50;
the plus sign printed in all three expansions on 53; every entry of slide 143's four matrices.
The parent's own check of two renders: slide 150 shows every matrix entry as transcribed (so the
143 slip is real), and slide 26 has 7 red and 15 blue points in both panels.

**Printed slips, transcribed as printed.** Slide 53 expands the hinge term as
W[j,:]·x **+** W[yᵢ,:]·x + 1 in all three places, where the score difference gives a minus; `[Ed:]`
line and wiki note. Slide 143's y = [[13, 9, -2, -6], [5, 2, 17, 1]] is not x·w =
[[-1, -1, 2, 6], [5, 2, 11, 7]] (only 5 and 2 agree), repeated on slides 144–150; `[Ed:]` line,
wiki note, INDEX rule and kb.json caveat. Recomputed and exact: the (x+y)z graph; every forward
value and gradient of the sigmoid graph (each printed value is the two-decimal rounding of the
step before; full precision gives -0.534, -0.197, 0.197 and a sigmoid gradient of 0.197); the
add, mul, copy and max gate values; the ReLU vectors; slide 144's ~256 GB (2^36 entries at 4
bytes is exactly 256 GiB).

**Transcript edit** (Sonnet, ~96k tokens). 99 paragraphs; marker sequence identical; word ratios
0.75–1.01. Number diff traced in full: "3264" was "32, 64" with the 32 already said (7:53); the
self-corrected "10 templates, 100 templates" kept as 100 (16:27); "x1 and y" → x and y (43:48);
three → 3 (44:35); "x 2" → x squared (54:39, 55:27); decimals at 56:12, 56:58, 57:44; "4,96" →
4096 (1:12:27). Parent fixes: at 20:25 the editor had turned the false start "for uh efficient" into
"their efficient models", now "their models"; the header said the hinge-loss digression had no
slide (slide 6 prints it) and cited a section map that did not exist. Restored names all appear in
the deck or in the captions (Swish, EfficientNet, polar coordinates and overfitting are in the
captions). Ten student-turn markers (17:59 answer; 22:46, 23:33, 25:53, 30:34, 32:06, 32:51,
33:37, 34:26, 52:22 questions); at 32:51 the captions carry the question in the clear, so it is
marked `*[Student question]*` without "inaudible". One `[unclear: 2]` at 1:00:04, where the slide
prints 0.2. **Coverage:** slides 3–4 and 12–21 are never presented; the recording ends at 1:16:19
at slides 151–152, with slides 143–150 in outline.

**Images.** 35 rendered (31 JPEG, 4 PNG; 5.2 MB): 13–21, 26, 30, 33, 34, 41, 42, 43, 46, 48, 49,
54–57, 74, 80, 96, 100, 104, 105, 116, 130, 137, 142, 150, 152. Not rendered: 1 (title); 3–4
(administrative); 5, 12, 22, 58, 59, 120, 151 (dividers and text); 6, 7, 11 (recaps of lecture 3
figures); 10 (animation frame); 8, 9, 23, 24, 27, 28, 31, 32, 36–40, 50–53, 115, 117–119,
121–123, 138, 144 (formulas, code and text transcribed exactly); build steps whose last step is
rendered (25 → 26, 29 → 30, 44–45 → 46, 60–73 → 74, 75–79 → 80, 81–95 → 96, 97–99 → 100, 101–103
→ 104, 106–111 → 105, 124–129 and 131 → 130, 132–136 → 137, 139–141 → 142, 143 and 145–149 → 150);
35 (slide 34's diagram beside code). The raster test flagged 111 of 147 pages with no recurring
template image; most of the gap to 35 is build steps and code screenshots. All 35 are in the
lecture page with hand-written captions; the topic pages carry 9 (neural-networks), 13
(backpropagation), 1 (regularization, slide 42) and 1 (gradient-descent, slide 54). Embed
problems, all fixed by moving the block: slide 33 landed between a sentence and its table, slide
42 between "in the regularized loss" and its formula, slide 104 (backpropagation page) between a
sentence and its list, and slide 105 in the sigmoid section because "printed on slide 105" there
was its first citation. Slides 80, 96, 130 and 150 were kept from the same problem by rewording
before the first embed.

**Wiki.** Lecture page: recording coverage and the two slips up front; administrative notes and
the "Today: Deep Learning" examples from the slides alone; the recap (with the lecturer's account
of the hinge loss and of Adam needing no manual decay); from linear classifiers to 2- and 3-layer
networks; non-linearity; templates; activation functions and the Q&A on choosing them;
architectures; the 20-line training loop; network size and regularization with the four student
questions (the lecturer's two practices, "a bit of a bigger network than we need" and "start with
smaller networks and increase", both recorded); biological neurons; computational graphs; both
worked examples with a value table; gate patterns; flat and modular implementations and PyTorch;
vectors, Jacobians, ReLU, matrices and the matrix-multiply gradients; summary. Two topic pages,
neural-networks and backpropagation.

### Run 4 checklist (moved verbatim from TODO.md)

Scope: lecture 4 only, video 25zD5qJHYsk (76:47). One deck, `lecture_4.pdf`: 147 pages, printed
1–152, 2, 47 and 112–114 absent (hidden slides; footer spans either side of each gap in the same
position, sequence monotonic); page 55 prints no number (a figure credit sits there), labelled 57.
Ehsan Adeli per the schedule. Images opted in (every figure-bearing slide). PDFs link-only.
Slug `04-neural-networks-backpropagation`.

#### Transcripts
- [x] 04 Neural Networks and Backpropagation — video 25zD5qJHYsk (original captions in raw/transcripts/original/; 99 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_4.pdf (title slide: "Lecture 4: Neural Networks and Backpropagation", April 10, 2025)
- [x] sources.md — the two handouts the schedule links by a broken relative path resolve at https://cs231n.stanford.edu/handouts/ (linear-backprop.pdf, derivatives.pdf: 200); record them

#### Slides (Step 1b)
- [x] raw/slides/04-neural-networks-backpropagation.md — number map, Sonnet transcription (four agents, pages 1–37 / 38–74 / 75–111 / 112–147), --verify (147 headings; exit 0)
- [x] Figure audit (Sonnet), two agents: slides 10, 11, 19, 25, 26, 30, 33, 41, 42, 46, 50, 53 and 74, 96, 100, 104, 105, 116, 134, 136, 143, 148, 152. Both rendered below the 600 dpi asked for (150 and 200 dpi, with crops at 400–600 dpi on 11, 53 and 116). Errors on 11 (step levels 1.4 / 1.05 → 0.95 / 0.9, one label, arrows end above the curve), 25–26 (7 red and 15 blue points, not 8 and ~16; red column right of the θ axis), small omissions on 41, 96, 116, 134. Confirmed: no paths on 10; no figure on 50; plus sign printed in all three places on 53; every matrix entry on 143. Fixes applied.
- [x] Worked arithmetic recomputed: (x+y)z, the sigmoid graph (forward and every gradient), the gates, the ReLU vectors and slide 144's 256 GB all exact; slide 143's printed y = [[13, 9, -2, -6], [5, 2, 17, 1]] is not x·w = [[-1, -1, 2, 6], [5, 2, 11, 7]] (confirmed on the page by the audit and on the slide 150 render) — [Ed:] line; slide 53's plus sign — [Ed:] line

#### Transcript edit (Step 1a)
- [x] raw/transcripts/04-neural-networks-backpropagation.md — Sonnet copy-edit; 99/99 markers identical; ratios 0.75–1.01; number diff: every difference traced (7:53 repeated "32" in "3264" dropped, 16:27 self-corrected "10 templates" dropped, 43:48 "x1" → x, 44:35 three → 3, 54:39 and 55:27 "x 2" → x squared, decimals at 56:12, 56:58, 57:44, 4,96 → 4096); parent fixes: 20:25 "their efficient models" (an insertion from the false start "for uh efficient") → "their models"; header said the hinge-loss digression had no slide (slide 6 prints it) and cited a nonexistent section map. Restored names all on the slides or in the captions (Swish, EfficientNet, polar, overfitting in the captions). 10 student-turn markers, 1 [unclear] (1:00:04). Recording skips slides 3–4 and 12–21; ends 1:16:19 at slides 151–152.

#### Images (Step 1c)
- [x] raw/images/04-neural-networks-backpropagation/ — select, render (35; 5.2 MB; 31 JPEG, 4 PNG), embed in slide file (35)
- [x] Embed in the wiki page (35, all with hand-written captions) and topic pages (neural-networks 9, backpropagation 13, regularization 1, gradient-descent 1); four blocks moved by hand (33, 42, 104 on the backpropagation page, 105)
- [x] Look at two rendered images against the slide-file claims (slide 150: every matrix entry as transcribed, so slide 143's slip is real; slide 26: 7 red and 15 blue in both panels, as the audit found)
- [x] INDEX.md image rules; AGENTS.md table row (and three general lessons: audit agents under-render; credit lines dropped by transcribers; the colon rule covers tables and code); BUILD_LOG.md render record; LICENSE.md attribution

#### Wiki
- [x] wiki/04-neural-networks-backpropagation.md (slips on slides 53 and 143 noted; slides 3–4 and 12–21 marked slide-only)
- [x] Topic pages: neural-networks, backpropagation; links from gradient-descent, linear-classifiers, regularization (new section on λ vs. network size), loss-functions, hyperparameters-and-validation, learning-rate-schedules, the 01, 02 and 03 pages, and the course-logistics roadmap (row 4; its stale "only lecture 1" sentence fixed)
- [x] INDEX.md table of contents (coverage 4 of 18; lecture 4 citation rule; skipped slides; printed-slips rule)

#### Publish
- [x] kb.json — coverage (4 of 18; 14 topic pages), decks 5/5, figure audit 5/5 (with lecture 4's low-dpi note), images 164 (byLecture 4: 35; 146 JPEG, 18 PNG), caveats for lecture 4 coverage, numbering and slips
- [x] BUILD_LOG.md — lecture 4 record
- [x] verify_kb.py clean, and its review section read (exit 0; all 1,412 formulas render in the chat and on github.com after fixing 8 `$$` blocks that GitHub set inline and slide 46's label list, which GitHub left as raw text; numeric claims in INDEX/AGENTS match the measured table; SEE_ALSO's "covers only Lecture 1" (stale since run 2) corrected)
- [x] Commit and push — 49b5274, 95a754d, 83c5db8 on https://github.com/chaimantec/cairn-kb-cs231n (INDEX, kb.json, lecture page, both topic pages, slide file, transcript and two images fetch 200 from raw.githubusercontent.com); kbUrl already set on the catalog entry since run 1
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 5 — Lecture 5 (Image Classification with CNNs), 2026-11-02

Built lecture 5 end to end: transcript, the deck, two figure audits, the transcript edit, the wiki
page, a convolutional-networks topic page, 53 slide images, and updates to INDEX, AGENTS, LICENSE,
kb.json, SEE_ALSO, the course-logistics roadmap (row 5 linked), neural networks (its "lecture 5 is
not covered" sentence replaced), image classification (a section on hand-designed features vs.
end-to-end learning), hyperparameters and validation (a lecture 5 section), linear classifiers,
loss functions (slide 129's slip), optimizers (the Adam Test of Time aside), ImageNet, computer
vision tasks, and the lecture 1 and 4 pages. Images opted in again; PDFs stay link-only.

### Lecture 5 record

**Deck.** One: `lecture_5.pdf`, 141 pages, Justin Johnson (per the schedule; he introduces
himself in the recording), April 15, 2025. Printed numbers 1–141, 1:1 with the pages: every page
prints its number in the "Lecture 5 - N" footer, and a scan of the bottom-of-page number spans
found no page out of sequence. No deck-wide licence. Per-image credits: slide 19 (Nikita, CC-BY
2.0), 26 and 34 (Krizhevsky, Sutskever and Hinton 2012, "Reproduced with permission"), 29–32
("Illustration of LeCun et al. 1998 from CS231n 2017 Lecture 1"), 35 (Ren, He, Girshick, Sun
2015 and Farabet 2012, "Reproduced with permission"), 36 (CC0, pixabay URLs; captions by Justin
Johnson with Neuraltalk2), 115 (PyTorch, BSD 3-clause), 133 (Rocky Acosta, CC-BY 3.0), 134
(Widrow 1960, with permission from Stanford University Special Collections), 135–137 and 140
(illustrations by Lane McIntosh, copyright CS231n 2017; 137 also Krizhevsky et al.), 138 (CNX
OpenStax, CC BY 4.0), 139 (retinotopy images courtesy of Jesse Gomez). Citations without a
licence line: 23 (Lowe 1999; Dalal and Triggs 2005), 24 (Fei-Fei and Perona 2005), 37 (Rombach et
al. 2022), 39–41 (Vaswani et al. 2017; Dosovitskiy et al. 2021), 69 (Springenberg et al. 2015),
141 (Fukushima 1980). "Slide inspiration: Justin Johnson" on 58–62 and 80–83. Schedule reading:
the Convolutional Networks course notes (cs231n.github.io/convolutional-networks), already in
`sources.md` with the deck.

**Transcription.** Four Sonnet agents in parallel (pages 1–36, 37–71, 72–106, 107–141), 74–85k
tokens each, all finished, every chunk appended as written. `--verify` clean (141 headings). The
parent fixed 24 GitHub math warnings (20 inline maths opened after a quote mark, a `_` after a
`}` in the PyTorch formula, math inside an italic `[Ed:]` line), escaped six digit asterisks
("5*5*3", "30*40*9") that GitHub would italicise, and removed the transcriber's architecture
names from slide 108 ("inception-style module", "residual-style network": the slide names
neither).

**Figure audit** (Sonnet, two agents, 24 slides). A: 4, 6, 22, 24, 26, 34, 35, 38, 62, 69, 80, 81.
B: 94, 101, 102, 108, 113, 118, 120, 124, 127, 129, 133, 136. Both rendered at 600 dpi but viewed
the pages downscaled to about 200 dpi; B cropped at true 600 dpi on 127, 129 and 133, A made no
crops (a `fitz` import failed under `python3 -I`). Errors: slide 4's timeline (World Labs to about
2026.5, axis to about 2028, navy teaching marks at about 2019.7, 2020.6 and 2022.6); 22 (bin 5 is
yellow-green, bar 7 medium); 24 (tall bars 1, 3, 4, 6, 9 in the top row, bar 4 tallest in the
bottom); 81 (the two blue input squares do not overlap: rows 1–3 / cols 1–3 and rows 5–7 / cols
5–7, and every square's position). Small fixes: 35 (one confidence blurry, 0.982 or 0.987, now
marked so), 38 (the title sits above the screenshot), 80 (dashed lines from two corners), 108
(maroon boxes; the "/ 2" on the last box of each group), 136 (the decoder continues upward).
Confirmed: 6's W, b, pixels and printed 61.95; 62's $C_{out}$ x $C_{in}$ x $K_w$ x $K_h$ order;
101's swapped labels; 102's grid; 124's "Conv layer" wording; every number on 127; the minus signs
on 129 (600 dpi crop); 133's formulas. The parent's own check of two renders: slide 101 shows the
swap as described; slide 81 matches the audit's positions except the second blue cell, which is
at row 6, column 6 (the centre of its square), not column 5.

**Printed slips, transcribed as printed.** Slide 6: the ship score 61.95 is the ship row times the
pixels without the bias; with $b = -1.2$ it is 60.75 (the same slip as lecture 2, slide 60, whose
figure the recap reuses). Slide 101: "64 x 112 x 112" over the larger cube and "64 x 224 x 224"
over the smaller, the reverse of the downsampling the figure shows; slides 18, 44, 100, 107 and
121 label it the right way round. Slide 124: "Conv layer needs 2 hyperparameters" under the
heading "Pooling layer: summary". Slide 129: the softmax loss with $e^{-s_y}$ and $e^{-s_i}$, which
would reward $s_y \to -\infty$, against the slide's own caption. Each has an `[Ed:]` line and a
wiki note; INDEX and kb.json list them. Recomputed and exact: HoG's 10,800 (slide 23); 28 and 24
(56, 64); 5×5 (75); 3×3 at stride 2 (86); 32, 760 and 768,000 (89, 91, 93); the max-pool output 6,
8, 3, 4 (102, 122); 28×28×5 (118); 1216 (127).

**Transcript edit** (Sonnet, ~96k tokens). 89 paragraphs; marker sequence identical; word ratios
0.80–1.02. Number diff traced in full: 30:42 false-start "3" and "372" dropped; 49:56 and 54:31
counts ("1 2 3 4 5", "1 2 3") written as words; 56:51 "2k + one" → 2K plus 1; 59:56 "64x12 x112",
"112 x12" (twice) and "224 x24" → 112 and 224 (the captions drop a digit after "x"; the lecturer
is reading slide 101's swapped labels); 1:00:44 and 1:02:15 "2x two" → 2 by 2, and a false-start
"two" before "4x4" dropped. Parent fixes: at 30:42 the editor had changed "that 32x32x3 vector"
to "tensor" (reverted); "760 multiple 760" (56:51) had become "760, multiply, 760", now
`[unclear: multiple]`; "it's a lot seven" (57:38) now `[unclear: it's a lot seven]`; the header
claimed no digit was changed in value and had no coverage note (both rewritten). Restored names
are on the slides or in the captions: LeNet ("lenat"), Inception, Stable Diffusion, MATLAB,
FLOPs, aspect ratio bucketing and Test of Time are in the captions; COVID is restored from "co" in
"what happened in 2020 other than co … it wasn't co, it was transformers". 19 student-question and
6 student-answer markers; 5 `[unclear]`. **Coverage:** the recording opens at 0:05 on slide 4,
never presents slides 2–3 or the appendix (109–141), and ends at 1:07:34 on slides 107–108.

**Images.** 53 rendered (34 JPEG, 19 PNG; 5.8 MB): 18, 20–26, 28, 31, 34–38, 41, 47, 50, 51,
55, 57, 60–62, 65, 67–69, 75, 79–81, 87, 97, 98, 101, 102, 106, 108, 114, 117, 118, 120, 127,
133–141. Not rendered: 1 (title); 2–3 (administrative); 4 (the lecturer's career timeline); 5,
15, 16 (outline); 6, 7, 9–14, 19, 66, 128–131 (recaps of lecture 2–4 figures); 8 (animation
frame); 42, 109 (dividers); 94, 95, 103, 111, 112, 115, 124, 125, 132 (text, formulas and
documentation screenshots transcribed exactly); 88–93 (the worked example's two unlabelled
slabs); build steps whose last step is rendered (17 → 18, 27 → 28, 29–30 → 31, 39–40 → 41, 46 →
47, 48–49 → 50, 52–54 → 55, 56 → 57, 58–59 → 60, 63–64 → 65, 71–74 and 76–77 → 75, 78 → 79,
82–83 → 81, 84–86 → 87, 104–105 → 106, 113 → 114); repeats of rendered figures (32, 33 → 31;
43–45, 99, 100, 107, 110 → 18; 70 → 65; 96 → 97–98; 116 → 51; 119 → 47; 121 → 101; 122–123 →
102; 126 → 120). The raster test flagged 66 of 141 pages (no recurring template image); it
missed the vector convolution diagrams (46–94) and flagged code and documentation screenshots.
All 53 are in the lecture page with hand-written captions; the convolutional-networks topic page
carries 6 (62, 65, 68, 81, 102, 106). One embed problem, fixed by moving the block: slide 75
landed between "a filter of width $K$," and its formula. The page's dimensions were first
written as plain "32×32×3", which check_math flags as notation (163 warnings): prose now uses
inline math, captions the slides' own "5x5x3".

**Wiki.** Lecture page: recording coverage and the four slips up front; administrative notes from
the slides; the lecturer; the recap (with the Adam Test of Time aside and the slide 6 slip); the
course's parts and the two new operators; hand-designed features (colour histogram, HoG, bag of
words from the slides only) vs. end-to-end learning; the spatial-structure problem; structure and
history to transformers, with the four reasons to still learn ConvNets; the fully connected layer
as template matching; the convolution layer and its eight questions; batches and general shapes;
the non-linearity exercise and the students' answers; what filters learn and four more
questions; output size and padding; receptive fields; stride; the worked example; the summary,
PyTorch and 1D/3D convolution; pooling, slide 101's slip and five questions; translation
equivariance; next time; the appendix slide by slide, with its change of notation ($K$ = number
of filters); summary. Topic page: convolutional networks.

### Run 5 checklist (moved verbatim from TODO.md)

Scope: lecture 5 only, video f3g1zGdxptI (68:04). One deck, `lecture_5.pdf`: 141 pages, printed
1–141, 1:1 (every page prints its number; no gaps). Justin Johnson per the schedule and the
recording. Images opted in (every figure-bearing slide). PDFs link-only.
Slug `05-image-classification-cnns`.

#### Transcripts
- [x] 05 Image Classification with CNNs — video f3g1zGdxptI (original captions in raw/transcripts/original/; 89 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_5.pdf (title slide: "Lecture 5: Image Classification with CNNs", April 15, 2025); already in sources.md

#### Slides (Step 1b)
- [x] raw/slides/05-image-classification-cnns.md — Sonnet transcription (four agents, pages 1–36 / 37–71 / 72–106 / 107–141), --verify (141 headings; OK); 20 inline-math-after-quote warnings and 4 others fixed
- [x] Figure audit (Sonnet), two agents: 4, 6, 22, 24, 26, 34, 35, 38, 62, 69, 80, 81 and 94, 101, 102, 108, 113, 118, 120, 124, 127, 129, 133, 136. Both viewed at ~200 dpi effective (600 dpi renders downscaled by the viewer); B cropped at 600 dpi on 127, 129, 133; A made no crops. Errors on 4 (timeline extents and marks), 22 (bin 5 colour, bar 7 height), 24 (which bars are tall), 81 (blue squares do not overlap; all square positions), small fixes on 35 (one confidence blurry: 0.982 or 0.987), 38, 80, 108, 136 (decoder runs upward). Confirmed: 6's matrices and printed 61.95; 62's K_w x K_h order; 101's swapped labels; 124's "Conv layer" wording; 127's numbers; 129's minus signs (600 dpi crop). Fixes applied.
- [x] Worked arithmetic recomputed: HoG 10,800 (23), 28 and 24 (56, 64), 5x5 (75), 3x3 (86), 32 (89), 76 and 760 (91), 768K (93), 28x28x5 (118), 1216 (127), 6/8/3/4 max pool (102, 122) all exact. Printed slips kept with [Ed:] lines: 6 (ship score omits the bias, as lecture 2 slide 60), 101 (cube labels swapped), 124 ("Conv layer" under the pooling heading), 129 (minus signs in the softmax exponents)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/05-image-classification-cnns.md — Sonnet copy-edit; 89/89 markers identical; ratios 0.80–1.02; number diff traced in full (30:42 false-start "3" and "372" dropped; 49:56 and 54:31 counts written as words; 56:51 "2k + one" → 2K plus 1; 59:56 "64x12 x112", "112 x12" ×2, "224 x24" → 112/224, the captions dropping a digit after "x"; 1:00:44 and 1:02:15 "2x two" → 2 by 2, false-start "two" dropped). Parent fixes: 30:42 "vector" had become "tensor" (reverted); 56:51 "multiply" guess → [unclear: multiple]; 57:38 → [unclear: it's a lot seven]; header listed no digit restorations and had no coverage (both written). Restored names in the slides or the captions (LeNet as "lenat", COVID as "co" in a 2020 aside, Inception, Stable Diffusion, MATLAB, FLOPs, aspect ratio bucketing all in the captions). 19 student-question and 6 student-answer markers, 5 [unclear]. Recording skips slides 2–3 and the appendix 109–141; ends 1:07:34 at slides 107–108.

#### Images (Step 1c)
- [x] raw/images/05-image-classification-cnns/ — select, render (53; 5.8 MB; 34 JPEG, 19 PNG), embed in slide file (53); header lists every unrendered slide and why
- [x] Embed in the wiki page (53, all with hand-written captions; slide 75 moved below its formula) and the convolutional-networks topic page (8: 62, 65, 81, 102, 106, 68 placed in the script's format); dimensions as inline math in prose and plain "5x5x3" in captions; unescaped digit asterisks (5*5*3) escaped in the page, the topic page and the slide file
- [x] Look at two rendered images against the slide-file claims (slide 101: labels swapped as the Ed line says; slide 81: square positions as corrected by the audit, except the second blue cell, which is row 6 column 6, not column 5 — fixed)
- [x] INDEX.md image rules (lectures 1–5; lecture 5 has 53); AGENTS.md table row (53 of 141); BUILD_LOG.md render record; LICENSE.md attribution (lecture 5 table and not-rendered note)

#### Wiki
- [x] wiki/05-image-classification-cnns.md (slips on slides 6, 101, 124 and 129 noted; slides 2–3 and the appendix 109–141 marked slide-only; slide 108's diagrams described unnamed, the transcriber's "inception-style"/"residual-style" glosses removed from the slide file)
- [x] Topic page convolutional-networks; links from neural-networks, image-classification (new section on hand-designed features), hyperparameters-and-validation (lecture 5 section), linear-classifiers, loss-functions (slide 129 slip), optimizers (Adam Test of Time aside), imagenet, computer-vision-tasks, the 01 and 04 pages, and the course-logistics roadmap (row 5)
- [x] INDEX.md table of contents (coverage 5 of 18; lecture 5 citation rule, skipped slides, four slips, slide 8's animation frame; lecture 5 and convolutional-networks entries; image-classification and hyperparameters one-liners; raw-materials lines); SEE_ALSO's "lectures 1–4" → 1–5

#### Publish
- [x] kb.json — coverage (5 of 18; 15 topic pages), decks 6/6, figure audit 6/6 (with lecture 5's ~200 dpi note), images 217 (byLecture 5: 53; 180 JPEG, 37 PNG), caveats for lecture 5's coverage, notation, numbering, slips and unclear marks
- [x] BUILD_LOG.md — lecture 5 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0; all 1,857 formulas render in the chat and on github.com after joining six inline formulas that wrapped across a line break, which only the --github pass caught, and fixing slide-62's extension on the topic page; numeric claims in INDEX/AGENTS match the measured table, lecture 5 53 on disk / 53 in wiki; AGENTS.md gains three general lessons: wrapped inline math, shape notation and digit asterisks; audit renders shown downscaled)
- [x] Commit and push — 7575c00, 54c3756, 978a327 on https://github.com/chaimantec/cairn-kb-cs231n (INDEX, kb.json, lecture page, topic page, slide file, transcript and two images fetch 200 from raw.githubusercontent.com); kbUrl already set on the catalog entry since run 1
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 6 — Lecture 6 (Training CNNs and CNN Architectures), 2026-11-02

Built lecture 6 end to end: transcript, the deck, two figure audits, the transcript edit, the wiki
page, five topic pages (CNN architectures, normalization layers, weight initialization, data
preprocessing and augmentation, transfer learning), 33 slide images, and updates to INDEX, AGENTS
(image row and one general lesson: count drawn architectures box by box), LICENSE, kb.json,
SEE_ALSO, regularization (dropout and the training-randomness pattern), neural networks (lecture
6's account of activation functions), hyperparameters and validation (the seven-step recipe,
accuracy curves, random search), ImageNet (the winners' depth), convolutional networks (stacked
3x3 receptive field; its "lecture 6 is not yet in this knowledge base" sentence replaced),
k-nearest neighbours (feature-space neighbours), image classification (frozen features), the
course-logistics roadmap (row 6 linked; its stale "lectures 1–4 are in this knowledge base"
corrected to 1–6), and the lecture 5 page's look ahead. Images opted in again; PDFs stay link-only.

### Lecture 6 record

**Deck.** One: `lecture_6.pdf`, 97 pages, Zane Durante (he introduces himself in the recording,
and mentions he gave lecture 3), April 17, 2025. Title slide "Lecture 6: Training CNNs and CNN
Architectures"; the catalog calls the lecture "CNN Architectures". Printed numbers 1–97, 1:1 with
the pages (`slide_number_map.py`: every page numbered, no gaps). No deck-wide licence. Credits and
citations: slide 6 "Slide inspiration: Justin Johnson"; 10–11 Ba, Kiros and Hinton 2016; 12 Wu and
He, ECCV 2018; 15 Srivastava et al., JMLR 2014; 25 Krizhevsky et al. 2012; 27 Hendrycks et al. 2016
and "Source: https://en.m.wikipedia.org/wiki/File:ReLU_and_GELU.svg"; 32–34, 44 the winners' papers;
35–43 Simonyan and Zisserman 2014; 45–57 He et al. 2015; 64–65 He et al., ICCV 2015; 75 DeVries and
Taylor, arXiv 2017; 80–82 Donahue et al. (DeCAF, ICML 2014) and Razavian et al. (CVPR Workshops
2014); 86 the torchvision and pytorch-image-models URLs; 95 Bergstra and Bengio 2012 and
"Illustration of Bergstra et al., 2012 by Shayne Longpre, copyright CS231n 2017". No "Reproduced
with permission" or CC line anywhere in the deck; the cat photographs (71–75) and the
nearest-neighbour grid (79) are uncredited.

**Transcription.** Three Sonnet agents in parallel (pages 1–33, 34–66, 67–97), 127–137k tokens
each, all finished, every chunk appended. `--verify` clean (97 headings). The parent fixed GitHub
math on slides 11 and 27 (inline math after a quote mark; math inside bold), later `x < 0` → `\lt`
on 28 and `\,` → `\thinspace` on 69–70 (both found only by the `--github` pass), tidied the
transcriber's own notes on 35 and 63, and added an `[Ed:]` line to 78.

**Figure audit** (Sonnet, two agents, 24 slides). A: 11, 12, 16, 27, 28, 32, 35, 41, 46, 49, 53,
57. B: 61, 63, 65, 71, 73, 75, 78, 79, 82, 85, 91, 95. Both rendered at 600 dpi but read most pages
downscaled (A about 110 dpi, B about 130 dpi); A cropped 35 and 41 at 300 dpi and 57 at 600; B
cropped 61, 63 and 65 at 600 dpi and 73 at 300. Errors: 35 (the transcriber drew three "3x3 conv,
256" boxes in VGG16 and four in VGG19; the page draws two in each, so the stacks count 15 and 17
weight layers, confirmed by the parent on the 1400px render); 41 (no blue square on A1 in the last
step); 73 (exactly four crop rectangles); 75 (grey-square positions); 78 (an 8x8 filter grid, not
8x7; the red box is on the 55x55x48 stage, not the input); 79 (the red box covers only the upper
2048 pair); 95 (the grid layout's three circles sit on the flat part and the two flanks, none at
the peak; guide lines in both plots). Small: 63's "all mass lies beyond the plotted range" was the
transcriber's inference (removed); 32's box positions added. Confirmed: 11's "Statistics
calculated per batch" (also in the text layer), 57's "3x3 conv, 64" top group (600 dpi crop and
the text layer), all 36 histogram means and stds on 61, 63 and 65, 85's four cells, 12's cells,
16's crossed-out features, 27–28's axes and formulas, 32's ten bars, 53's stack. Parent check of
two renders: slide 35 (diagram) agrees with the audit; slide 32 (chart) agrees with the file.

**Printed oddities, transcribed as printed.** Slide 11: "Statistics calculated per batch" points
at μ, σ: N x 1, one pair per sample (the lecturer describes per-sample statistics, 4:45–5:31).
Slide 35: VGG16 and VGG19 stacks draw 12 + 3 and 14 + 3 weight layers. Slide 57: the last group is
labelled "3x3 conv, 64"; slides 53–56 print 512. Slides 78–79: "(More on this in Lecture 13)";
in the 2025 schedule lecture 13 is Generative Models 1 and visualizing is in lecture 9. Each has an
`[Ed:]` line and a wiki note; INDEX and kb.json list them. Recomputed and exact: 28x28 (6), the
max and average pools (7), 2^4096 ~ 10^1233 (17), the 7x7 receptive field (37–42), 27C² vs. 49C²
(43), 10 test crops (73). The lecturer's spoken "0.022" for the right scale matches sqrt(2/4096) =
0.0221. Slide 19's code defines p as the probability of keeping a unit while the lecturer says
"probability of dropout" (same number at 0.5); the wiki states both.

**Transcript edit** (Sonnet). The agent hit the session's usage limit after writing the whole file
and its final header, before it could report; the parent checked the file as written. 93
paragraphs; marker sequence identical; word ratios 0.73–1.03, the low one 1:01:37, where the
captions repeat "say" 61 times (collapsed, with an `[Ed:]` note). Number diff: 20:06 caption "5x"
→ Phi (the Gaussian CDF; listed); 1:01:37 "60" added inside the Ed note. Restored names: GELU,
SiLU, AlexNet, ImageNet, LayerNorm, ResNet, Kaiming, Phi are on the slides; Zane Durante, Ehsan,
Fei-Fei are the course staff; LoRA ("Laura") and Ed ("Edge") are spoken only. 22 student-question
and 4 student-answer markers, 2 "Student, partly audible" (7:48, 8:35), 2 `[unclear]` plus the Ed
note. **Coverage:** the recording opens at 0:05 with the introduction and the overview (slide 3),
never presents slide 2, follows the deck to the summary and ends at about 1:10:50; at 51:34 a
question returns to weight initialization, and 1:04:40–1:06:59 answer questions on LoRA and on
ResNet's paired convolutions with no slide.

**Images.** 33 rendered (13 JPEG, 20 PNG; 3.9 MB): 8, 12, 15, 16, 24, 26, 27, 28, 32, 35, 41, 47,
49, 52, 54, 55, 57, 61, 63, 65, 71, 72, 73, 74, 75, 78, 79, 82, 85, 90, 92, 93, 95. Not rendered: 1
(title); 2 (logistics); 3–5, 20, 31, 58, 66, 68, 76, 87 (overview); 6, 7 (lecture 5 recaps,
values transcribed); 59 (divider); 10, 11, 17, 18, 19, 45, 48, 60, 62, 64, 67, 69, 70, 77, 86, 88,
89, 94, 96, 97 (text, equations and code transcribed exactly); build steps whose last step is
rendered (9, 13, 14, 21, 22 → 8; 23 → 24; 25 → 26; 29–30 → 28; 33, 34, 44 → 32; 37–40 → 41; 46 →
47; 50–51 → 52; 80–81 → 82; 83–84 → 85; 91 → 92); repeats with transcribed text (36, 42, 43 → 35;
53, 56 → 54–55). The raster test flagged 36 of 97 pages; it missed the vector diagrams (stacks,
receptive-field grids, residual blocks) and flagged pasted equations. All 33 are in the lecture
page with hand-written captions; the topic pages carry 31 more embeds (cnn-architectures 8,
normalization-layers 2, weight-initialization 3, data-augmentation 5, transfer-learning 4,
regularization 3, hyperparameters-and-validation 4, imagenet 1, k-nearest-neighbors 1), captioned
from the lecture page's captions. One embed problem, fixed by moving the block: slide 85 landed
between "fill in a table … :" and its table (lecture page); on the transfer-learning page the
sentence was rewritten to follow the table instead.

**Wiki.** Lecture page: recording coverage and the four oddities up front; administrative notes
from slide 2; the lecturer; the two sets of topics; the convolution and pooling recap; the
components of a CNN; normalization layers (the two steps, LayerNorm and its shapes, the four-way
comparison and its Q&A); dropout (the idea, redundant representations, the ensemble view, the Q&A,
test-time scaling and slide 19's keep-probability p); activation functions (sigmoid, ReLU, GELU and
SiLU, the zoo, where they go); CNN architectures (the winners chart, AlexNet and VGG, the receptive
field and parameter count, the plain-network degradation, residual blocks, the full ResNet, the
Q&A); weight initialization (the three experiments, Kaiming, the Q&A including the 51:34 return);
data preprocessing; data augmentation; transfer learning (features, the three steps, bias, the
table, LoRA, model zoos); choosing hyperparameters (the recipe, the curves with the lecturer's
"loss"/"accuracy" slip noted, random vs. grid); summary.

### Run 6 checklist (moved verbatim from TODO.md)

Scope: lecture 6 only, video aVJy4O5TOk8 (71:07). One deck, `lecture_6.pdf`: 97 pages, printed
1–97, 1:1. Title slide "Lecture 6: Training CNNs and CNN Architectures", April 17, 2025; Zane
Durante (introduces himself in the recording). Images opted in (every figure-bearing slide). PDFs
link-only. Slug `06-training-cnns-architectures`.

#### Transcripts
- [x] 06 Training CNNs and CNN Architectures — video aVJy4O5TOk8 (original captions in raw/transcripts/original/; 93 paragraphs)

#### Crawl
- [x] Deck fetched by hand into raw/pdfs/slides/lecture_6.pdf (title slide checked); already in sources.md

#### Slides (Step 1b)
- [x] raw/slides/06-training-cnns-architectures.md — Sonnet transcription (three agents, pages 1–33 / 34–66 / 67–97, all finished, chunks appended), --verify (97 headings; OK); parent fixed four GitHub-unsafe maths on slides 11 and 27, tidied two transcriber notes (35, 63), added the "Lecture 13" Ed line (78)
- [x] Figure audit (Sonnet), two agents: 11, 12, 16, 27, 28, 32, 35, 41, 46, 49, 53, 57 and 61, 63, 65, 71, 73, 75, 78, 79, 82, 85, 91, 95. Both rendered at 600 dpi but read most pages downscaled (~110–130 dpi); crops of 35, 41, 73 at 300 dpi and 57, 61, 63, 65 at 600 dpi. Corrections: 35 (each VGG stack draws two "3x3 conv, 256" boxes, not three/four), 41 (no blue square on A1), 63 (an inference removed), 73 (four rectangles), 75 (square positions), 78 (8x8 grid; red box position), 79 (red box on the upper 2048 pair only), 95 (grid circles on the flat part and flanks, none at the peak; guide lines in both plots); 32 box positions added. Confirmed: 11 "Statistics calculated per batch" (also text layer), 57 top group "3x3 conv, 64" (600 dpi crop and text layer), every histogram mean/std on 61/63/65, 85's cells. Parent check of slide 35 on its 1400px render agrees with the audit.
- [x] Worked arithmetic recomputed: 28x28 (6), pooling (7), 2^4096 ~ 10^1233 (17), 7x7 receptive field (37–42), 27C^2 vs 49C^2 (43), 10 crops (73) all exact; sqrt(2/4096) = 0.0221 matches the lecturer's spoken "0.022". Printed oddities kept with [Ed:] lines: 11 ("per batch" for N x 1 per-sample statistics), 35 (VGG16/VGG19 stacks draw 15 and 17 weight layers), 57 (last group labelled 64, slides 53–56 print 512), 78–79 ("Lecture 13"; visualizing is lecture 9 in 2025)

#### Transcript edit (Step 1a)
- [x] raw/transcripts/06-training-cnns-architectures.md — Sonnet copy-edit (the agent hit the session limit after writing the whole file and header, before its report); 93/93 markers identical; ratios 0.73–1.03 (0.73 is 1:01:37, the 61-times "say" caption glitch collapsed with an Ed note); number diff: 20:06 "5x" → Phi (listed), 1:01:37 "60" added in the Ed note. Restored names in the slides or the course staff list (Ehsan, Fei-Fei, Zane Durante); LoRA spoken only. 3 [unclear] (17:00, 27:45, 1:01:37 note), 2 "Student, partly audible" (7:48, 8:35)

#### Images (Step 1c)
- [x] raw/images/06-training-cnns-architectures/ — rendered 33 (13 JPEG, 20 PNG; 3.9 MB); embedded in the slide file (33); header lists every unrendered slide and why
- [x] Embed in the wiki page (33, all with hand-written captions; slide 85 moved below its table) and nine topic pages (31: cnn-architectures 8, normalization-layers 2, weight-initialization 3, data-augmentation 5, transfer-learning 4, regularization 3, hyperparameters 4, imagenet 1, k-NN 1), captions taken from the lecture page
- [x] Look at two rendered images against the slide-file claims (slide 35 diagram: agrees with the audit, two 256 boxes per VGG stack; slide 32 chart: values, boxes and triangles as the file says)
- [x] INDEX.md image rules (lectures 1–6; lecture 6 has 33); AGENTS.md table row (33 of 97); BUILD_LOG.md render record; LICENSE.md attribution (lecture 6 table and not-rendered note)

#### Wiki
- [x] wiki/06-training-cnns-architectures.md (four printed oddities noted: 11, 35, 57, 78–79; slide 2 slide-only; the 51:34 detour and the LoRA / paired-convolution answers marked; slide 19's keep-probability p vs. the spoken "probability of dropout"; the spoken "loss" for the accuracy curves)
- [x] Topic pages cnn-architectures, normalization-layers, weight-initialization, data-augmentation, transfer-learning; sections or links in regularization (dropout, the randomness pattern), neural-networks (lecture 6 activations), hyperparameters-and-validation (lecture 6 section), imagenet, convolutional-networks ("not yet in this knowledge base" replaced), k-nearest-neighbors, image-classification, course-logistics (row 6; stale "lectures 1–4" fixed), lecture 5 page
- [x] INDEX.md table of contents (coverage 6 of 18; lecture 6 citation rule, skipped slide, four oddities; lecture 6 and five topic entries; seven one-liners updated; raw-materials lines); SEE_ALSO "lectures 1–6"

#### Publish
- [x] kb.json — coverage (6 of 18; 20 topic pages), decks 7/7, figure audit 7/7 (lecture 6 note), images 250 (byLecture 6: 33; 193 JPEG, 57 PNG), caveats for lecture 6's coverage, numbering, oddities and unclear marks
- [x] BUILD_LOG.md — lecture 6 record and index row
- [x] verify_kb.py clean, and its review section read (exit 0 after fixing six GitHub math problems the --github pass found: two inline maths wrapped across a line break, a `$...$` followed by ")", `x < 0` and two `\,` in the slide file; 2,055 formulas render in both; numeric claims in INDEX/AGENTS match the measured table, lecture 6 33 on disk / 33 in wiki; AGENTS.md gains one general lesson: count drawn architectures box by box)
- [x] Commit and push — cc11465, 15e39a3, 7ed2cb1 on https://github.com/chaimantec/cairn-kb-cs231n (INDEX, kb.json, lecture page, topic page, slide file, transcript and two images fetch 200 from raw.githubusercontent.com); kbUrl already set on the catalog entry since run 1
- [x] Move this run's finished sections to BUILD_LOG.md; TODO.md keeps only open work

## Run 7 — Lecture 7 (Recurrent Neural Networks), 2026-11-02

Built lecture 7 end to end: transcript, the deck (four transcription agents), two figure audits
(one extended to the min-char-rnn listing), the transcript edit, the wiki page, four topic pages
(recurrent neural networks, LSTM, character-level language models, image captioning and visual
question answering), 43 slide images, and updates to INDEX, AGENTS (image row and one general
lesson: code listings pasted as images have no text layer, so values a slide file quotes from one
go into the audit), LICENSE, kb.json, SEE_ALSO, regularization (lecture 7's dropout-$p$
clarification), normalization layers (the LayerNorm vs. initialization experiment, with slide 7),
weight initialization, backpropagation (through time), computer vision tasks (captioning), CNN
architectures (the LSTM parallel), transfer learning (captioning's CNN encoder), hyperparameters
and validation (Weights and Biases, with slide 12), neural networks (tanh in RNNs), loss functions
(per-step softmax), course logistics (row 7; "lectures 1–7"), and the lecture 6 page (forward
pointer from its dropout passage; next-lecture link). Images opted in again; PDFs stay link-only.

### Lecture 7 record

**Deck.** One: `lecture_7.pdf`, 124 pages, April 22, 2025, title slide "Lecture 7: Recurrent Neural
Networks". The lecturer is Zane Durante: he opens with clarifications of "when I gave lecture last
time" (lecture 6). Printed numbers 1–133 with 19, 20, 52, 53, 71, 72, 73, 100 and 103 absent; page
118 prints no number (127, between 126 and 128; `slide_number_map.py` marks it inferred). No
deck-wide licence. Credits and citations: slide 4 Srivastava et al., JMLR 2014; 12 the wandb docs
URL; 67 the min-char-rnn gist URL and "Written by Andrej Karpathy (@karpathy) BSD License"; 68
"Blogpost from Andrej Karpathy back in 2015!"; 76 the openai-codex URL; 78–83 Karpathy, Johnson and
Fei-Fei, ICLR Workshop 2016, "Figures copyright Karpathy, Johnson, and Fei-Fei, 2015; reproduced
with permission"; 85 "Figure from Karpathy et a, … CVPR 2015; figure copyright IEEE, 2015.
Reproduced for educational purposes."; 87 "This image is CC0 public domain"; 97–98 neuraltalk2 and
CC0 image credits; 99 Agrawal et al. ICCV 2015, Zhu et al. CVPR 2016, "Figure from Zhu et al,
copyright IEEE 2016. Reproduced for educational purposes."; 101 Das et al. CVPR 2017, "Figures from
Das et al, copyright IEEE 2017. Reproduced with permission."; 102 Wang et al. CVPR 2018, "Figures
from Wang et al, copyright IEEE 2017. Reproduced with permission." (year as printed); 105–119
Hochreiter and Schmidhuber 1997; 106–117 Bengio et al. 1994 and Pascanu et al. 2013; 120–130
"[Hochreiter et al., 1997]"; 130 Srivastava et al., Highway Networks, 2015; 131 "RWKV Scaling
(arXiv)" and the S5 and Mamba paper titles.

**Transcription.** Four Sonnet agents in parallel (pages 1–31, 32–62, 63–93, 94–124), 130–133k
tokens each, all finished, every chunk appended. `--verify` clean (124 headings). The parent
fixed GitHub math on slides 31, 34, 85, 119, 121 (a space inside `$`, math after a quote mark, a
closing `$` before ")", `_` after `}`) and rewrote the `[Ed:]` lines on 66, 106 and 110 without
math (GitHub does not render math inside italics). Slide 67's transcriber called the listing "too
small to read at slide size" yet quoted hyperparameters and lines from it; the code is a raster
image with no text layer, so the parent sent it to the audit, which confirmed every quoted item on
600 dpi crops.

**Figure audit** (Sonnet, two agents, 27 slides). A: 7, 12, 23, 33, 54, 56, 58, 61, 62, 64, 65, 66,
crops of 600 dpi renders for 7, 12, 61, 62, 64, 65, 66 (23, 33, 54, 56, 58 from ~150 dpi page
views). B: 85, 88, 91, 97, 98, 99, 104, 111, 113, 116, 120, 125, 129, 131, then 67; crops of 600 dpi
renders (pdftoppm) for 85, 88, 91, 111, 113, 116, 120, 125, 129, 131, 99 (questions 3–4) and six
strips of 67 (97, 98, 99's first two questions and 104 from ~150 dpi views). Corrections: 7 (orange
and red start values in the train panel), 58 (the grey box also encloses the output box), 61 (the
"target chars:" label is black), 88 (20 boxes, 10 conv + 3 FC = 13 weight layers; the transcriber
listed all ten conv boxes but counted eight), 131 (a missing Pythia point; OPT's last point).
Confirmed: every hidden, output, softmax and embedding vector on 61–66 (slide 66's third and fourth
embeddings are identical; both inputs are "l"), slide 66's w14 rows, 67's listing, 85's labels,
91's equations, 111's lowercase $t$, 113's equation and chart, 116's code (no square root), 120's
size labels, 125's arrows, 129's labels and arcs (last group "3x3 conv, 64"). Parent check of two
renders: slides 65 and 66 agree with the audit (the slips are printed).

**Printed slips, transcribed as printed.** Slide 65: softmax columns 1 and 2 printed
(.03, .84, .00, .13) and (.25, .20, .50, .05); the printed scores (1.0, 2.2, -3.0, 4.1) and
(0.5, 0.3, -1.0, 1.2) give (.038, .125, .001, .837) and (.247, .202, .055, .497); columns 3 and 4
recompute exactly. The lecturer acknowledges it: "This is incorrect, actually … no one noticed it"
(38:42) and "imagine the probabilities are correct here" (43:21). Slide 66: rows 2 and 3 end in
w14. Slide 106: W_xh then W_hx. Slide 110: lowercase t in the chain from T. Slide 116: `grad_norm =
np.sum(grad * grad)` is the squared norm. Slide 129: ResNet's last stage "3x3 conv, 64" (lecture 6,
slide 57's figure). Each has an `[Ed:]` line and a wiki note; INDEX and kb.json list them. The
hand-built repeated-1s RNN (29–38) recomputes exactly.

**Transcript edit** (Sonnet). 93 paragraphs; marker sequence identical; word ratios 0.76–1.02.
Number diff: 13:15 "10h" → tanh, 15:36 "001" → "0 0 1", 17:08 "one" → "1" (all listed); 45:39
"minus one" → "minus 1" twice, unlisted, reverted by the parent. The parent corrected three header
claims: Karpathy is on slides 67–68 (the editor called him spoken-only and added "former course
instructor" as its own gloss; the lecturer does say "a former instructor of this course" at 39:30),
and "four gates" / "gate gate" are printed on slides 119 and 121–124, not 125. Restored names are on
the slides or are the course staff; TensorBoard, RoPE and beam search are spoken only. 13
student-question, 2 student-answer and 5 partly-audible markers; 3 `[unclear]`.
**Coverage:** opens at 0:05 with the clarifications (slides 3–10), never presents slide 2, follows
the deck to the summary and ends shortly after 1:11:03. The chunked-backpropagation answer
(31:48–35:36) describes carrying a gradient across chunk boundaries with one update per chunk,
which slides 56–58 do not draw and which differs from the lecturer's own 28:44 "the gradients are no
longer carrying over"; the wiki reports both. The interpretable-cell colour code (−1 red, +1 blue)
is spoken only (45:39).

**Images.** 43 rendered (29 JPEG, 14 PNG; 5.0 MB): 7, 12, 18, 22, 26, 28, 42, 45, 47, 50, 51, 54,
57, 58, 61, 65, 66, 68, 74, 76, 77, 78, 79, 80, 81, 82, 83, 85, 96, 97, 98, 99, 101, 102, 104, 108,
113, 116, 124, 125, 126, 130, 131. Not rendered: 1 (title); 2 (logistics); 3, 11, 13, 84, 128, 132,
133 (overview, recap, text); 4 (recap of lecture 6's dropout figure); 5, 6, 24, 25, 27, 29–38, 105,
118, 119 (text, equations, code and the X/Y table transcribed exactly); 67 (code listing,
summarised); 69, 70, 75 (generated text transcribed); build steps whose last step is rendered (8–10
→ 7; 14–17 → 18; 21 → 22; 23 → 26; 39–41 → 42; 43–44 → 45; 46 → 47; 48–49 → 50; 55–56 → 57; 59–60 →
61; 62–64 → 65; 86 → 85; 87–95 → 96; 106–107 → 108; 109–112 → 113; 114–115 → 116; 120–123 → 124;
127, 129 → 130); 117 (repeat of 116's figure with text transcribed). The raster test flagged 89 of
124 pages (code images, equations, generated text, build steps) and missed 12 vector diagrams that
were rendered (22, 26, 42, 45, 47, 50, 51, 54, 57, 58, 77, 104). All 43 are in the lecture page with
hand-written captions; the topic pages carry 27 more embeds (recurrent-neural-networks 7, lstm 4,
language-models 7, image-captioning 7, normalization-layers 1, hyperparameters-and-validation 1).
The images were placed by hand and the embed script run afterwards (it found nothing to add in the
wiki); every image was first linked as `.jpg`, so the 14 PNGs had to be corrected from the files on
disk. Captions were first written with inline math, which GitHub does not render inside italics;
they were converted to plain text (Unicode subscripts, "4h x 2h").

**Wiki.** Lecture page: lecturer, coverage and the six slips up front; administrative notes from
slide 2; the two clarifications (dropout's $p$; the LayerNorm vs. initialization experiment);
recap and Weights and Biases; sequence shapes; the recurrence, unrolling and the vanilla RNN, with
the Q&A; the hand-built repeated-1s RNN with its weight matrices; computational graphs (many to
many, many to one, one to many), backpropagation through time, truncated, the single-output case
and the chunking Q&A; the character-level language model, sampling (slide 65's slip and the
lecturer's acknowledgement), greedy decoding and beam search, the embedding layer (the lecturer's
"row" vs. the slide's "column"); min-char-rnn and generated text; interpretable cells; tradeoffs;
captioning (the CNN drawn on 88–96 counted box by box), results and failures, VQA, visual dialog,
navigation; multilayer RNNs; gradient flow (the lecturer's "diagonally positioned … zeros" vs.
slide 106's side-by-side blocks), clipping (the squared norm); the LSTM, its gates, cell diagram,
gradient flow, slide 128, ResNet and Highway Networks; modern RNNs; summary.

