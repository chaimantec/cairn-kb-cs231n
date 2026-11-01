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

