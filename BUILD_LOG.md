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

