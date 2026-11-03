# How this knowledge base is organized

This repo is the knowledge base for **CS231N — Deep Learning for Computer Vision, Stanford,
Spring 2025** (Fei-Fei Li, Ehsan Adeli). It is read by Cairn's in-extension AI chat, which starts
at `INDEX.md`, fetches files over raw.githubusercontent.com and follows relative markdown links.

The chat never reads this file. It is for whoever builds the KB, and Claude Code
loads it into every step of every build agent, so keep it to the rules every
lecture's build follows. The per-lecture record (licence notices, audit findings,
printed slips, which slides were rendered and why) goes in
[`BUILD_LOG.md`](BUILD_LOG.md); anything the chat needs goes in `INDEX.md`.

## Layout

| Path                | Contents                                                      |
| ------------------- | ------------------------------------------------------------- |
| `INDEX.md`          | Entry point. Course summary, coverage, citation and image rules, annotated table of contents. |
| `wiki/`             | Durable pages: one per lecture (`NN-<slug>.md`), plus cross-lecture topics. |
| `raw/slides/`       | Full text of every slide. One file per deck: `NN-<slug>.md`, or `NN-<slug>-part-K.md` when a lecture has several decks. Headings use the **printed** slide number. |
| `raw/transcripts/`  | Copy-edited transcripts with `[M:SS]` paragraph marks. The chat reads these. |
| `raw/transcripts/original/` | Verbatim auto-captions. **Gitignored**, local reference only (no licence; a full caption copy is the weakest thing to publish). Regenerable from the video id. |
| `raw/images/`       | Rendered figure slides, one directory per deck, named like the slide file. |
| `raw/pdfs/`         | Downloaded decks. **Gitignored**; linked at their canonical URLs instead. |
| `sources.md`        | Crawl inventory: canonical URL of every course document.     |
| `LICENSE.md`        | Licence layers, and the attribution of every rendered image. |
| `SEE_ALSO.md`       | Sibling KBs the chat may consult (`kb` argument).           |
| `kb.json`           | Machine-readable coverage and provenance. Update with every run. |
| `TODO.md`           | Open work only. Finished runs move to `BUILD_LOG.md`.       |
| `BUILD_LOG.md`      | Finished runs, one section each. Not needed to answer questions. |

## Conventions

- **INDEX.md is the front door.** The chat reads it first on every conversation.
  Every wiki page must appear there with a one-line description of what it holds.
  An unindexed page is effectively invisible. Keep its coverage line ("N of 18 lectures")
  and its list of lectures with images true after every run.
- **Relative links only**, including to images. Slide PDFs are not committed, so link decks at
  their canonical `https://cs231n.stanford.edu/slides/2025/…` URL, never `../raw/pdfs/…`.
- **Cite everything.** Claims trace back to a transcript timestamp `(≈M:SS)` or a slide.
- **Several decks per lecture.** Lecture 1 has two decks, both numbered from 1. Cite them
  "part 1, slide N" / "part 2, slide N" everywhere in the wiki — never a bare "slide N" — and
  embed their images with `embed_slide_images.py --deck-label "Part K"`, which anchors only on
  citations carrying that label. Without the label a part-1 image lands beside a part-2
  citation of the same number.
- **Never invent course content.** If the transcript is unclear at some point,
  say so on the page. Do not fill the gap from outside knowledge — the chat
  presents these pages as authoritative material from this course. That includes plausible
  glosses a transcriber adds, such as calling an untitled chart axis "top-5 error": check
  slide-file inferences before they reach the wiki. It also covers questions a deck poses
  without printed answers (lecture 2's SVM quiz slides): state the question, say no answer is
  printed, and do not supply one.
- **Count drawn architectures box by box.** Transcribers normalise a diagram toward what its name
  leads them to expect (lecture 6: an extra conv box in each VGG stack, so the drawing seemed to add
  up to 16 and 19 layers). Have the audit count every box on a crop; when the drawn count disagrees
  with the name, transcribe the drawing and add an `*[Ed: …]*` line. Read a slide's words against
  its own drawing the same way: lecture 11's "shard first over row and second over column" names the
  opposite of the column and row blocks it draws.
- **Recompute worked arithmetic on the slides.** Decks print slips in their own worked examples
  (a score missing its bias term, a log in a different base from the rest of the deck). Keep the
  printed value, add an `*[Ed: …]*` line under the slide in the slide file, and say it on the
  wiki page; never silently correct it.
- **Prose over fragments.** The chat quotes these pages to learners; bullet
  fragments quote badly. Lists that cite rendered slides also stack every image after the
  list (the embed script never inserts inside a list), so write those passages as short
  paragraphs, one per cited slide.
- **Recordings can skip slides.** Lecture 1's recording skips the logistics slides. When that
  happens, say so in the slide file's header, the transcript header and the wiki page, so the
  slide file is known to be the only source.
- **Math in LaTeX**: `$...$` inline, `$$...$$` displayed, never inside a code fence. Define each
  symbol on first use and follow the slides' notation. Run `check_math.mjs` (via
  `verify_kb.py`) before publishing. Never let an inline `$...$` wrap across a line break (GitHub
  shows it as raw text; only the `--github` pass catches it). Write tensor shapes in prose as math
  (`$32 \times 32 \times 3$`, not "32×32×3", which the checker flags), and in italic captions,
  where math does not render on GitHub, as the slides print them ("5x5x3"). Escape a `*` between
  digits ("5\*5\*3"), or GitHub italicises the middle digit. A notation pass over a slide file
  converts labels, not printed prose: lecture 11's list text prints a plain "dL/dW_i" where its
  figure labels print ∂, and a blanket conversion made both ∂ until a render showed it.
- **Transcripts keep the spoken form.** No LaTeX in `raw/transcripts/`; notation is reconstructed
  in `wiki/`.

## Sources and numbering

- **Fetch decks by hand.** The course site's pages live under `/2025/` but its decks under
  `/slides/2025/`, outside the crawler's path prefix, so `crawl_course_site.py` records them as
  off-site links and downloads none. `curl` each lecture's deck into `raw/pdfs/slides/`, then
  mark `cs231n.stanford.edu` documents on-site in the inventory before rendering `sources.md`.
  A schedule row can link a deck from the 2024 archive; check its title slide.
- **Slide numbers are printed mid-footer**, as a separate text span after "CS231n: Lecture N -"
  (or "Lecture N -"), neither in a corner nor centred. `slide_number_map.py` reads this as its
  split-footer case. A few pages that drop the footer print the number bare in the bottom-right
  corner instead. Decks hide slides: lecture 1 part 2 is missing printed numbers 4, 5 and 45.
  The number span can overlap the "Lecture N -" span (lecture 2 page 32); the script handles
  that now, but a single page reading a small number out of sequence is a misread, not a hidden
  slide: check the raw spans before handing the map to agents.
- Each deck prints per-image credit lines (CC licences, public domain, "Figures copyright …
  Reproduced with permission"). Grep the text layer for them to write `LICENSE.md`, and check each is in the slide file
  (transcribers drop them); permission
  granted to the course does not pass to this repo, and `LICENSE.md` says so.

## Transcripts

- Copy-edit with a Sonnet agent against the finished slide files, then check in the parent:
  identical `[M:SS]` sequence, number inventory of the bodies, per-paragraph word ratio
  (0.72–1.10), and a grep of every restored proper noun against the slide files and the
  original captions. Trace every number difference the editor did not list to its paragraph:
  an unlisted "2" in lecture 2 was an interpretive insertion ("there" became "with L2").
  Read every ratio outlier against the original yourself, whatever the editor says about it: an
  outlier reported as filler removal can be a sentence moved across the marker (lecture 8).
  Then list, per paragraph, the words the edit introduced that the original paragraph lacks, and
  read each: substitutions pass every other check (lecture 9: "routed to a of those e experts",
  slide 27's A of E, became "a few of those experts"; "over fine-tune" became "overfit"), including a
  correctly heard word changed to the one the context expects (lecture 12: "perturbations" became
  "permutations"). The same
  sweep catches a few words moved across a marker at a paragraph boundary, which leaves both ratios
  in band (lecture 10: the first words of two paragraphs had been pulled back into the paragraph
  before). Then check every quotation the wiki takes from the transcript against it verbatim.
- Student turns: only the lecturer is audible; mark `*[Student question, inaudible]*` /
  `*[Student answer, inaudible]*` where the captions show a speaker change.

## Images

**Lectures 1–12 have images; no other lecture does yet.** They are committed rather than hotlinked, and
they are the only part of this KB that redistributes course material rather than describing it.

- Render every slide that carries a figure, by printed number, with `extract_slide_images.py`
  (1400px, `--format auto`, so a few vector slides come out `.png`). Skip title, agenda and
  divider slides; text-only slides; tables the slide file reproduces exactly; build steps and
  recaps that repeat a rendered figure; animation frames (below); and photographs of course
  staff, guest lecturers and award winners.
- The raster test over-reports on these decks (part 1 carries a full-page template image on
  every page; exclude images that recur on most pages; code listings and equations are often
  pasted in as images) and under-reports vector charts and diagrams (Venn builds, GFLOP charts).
  Use the slide file's prose as the deciding signal.
- **Audit agents under-render.** Figure-audit agents have rendered at 150–200 dpi when asked for
  600 and said so only in passing; even a true 600 dpi page render is shown to them downscaled to
  about 200 dpi, so only crops are read at full resolution. Ask for crops of every value checked.
  Code listings pasted in as images have no text layer: when a slide file quotes lines or values
  from one (lecture 7's min-char-rnn, described as too small to read yet quoted in detail), put it
  in the audit. Read each report's method line, and confirm any value the wiki
  will quote as a correction (a printed slip, a matrix) on the 1400px render as well. On drawn
  (vector) slides the text layer's span positions settle layout exactly (which grid row is on top,
  where a label sits): check a disputed or self-contradictory audit claim there before
  re-auditing. A pasted-in copy of the same diagram has no such layer and may be drawn the other
  way up (lecture 8).
- **Decks hold animation frames and video stills.** A slide whose animation drew paths or builds
  exports to the PDF as its background frame only (lecture 3's optimizer comparisons: a loss
  surface and a legend, no paths), and an embedded video as one still (lecture 10). Confirm the
  absence at 600 dpi in the figure audit, say so in the slide file's header and on the wiki page,
  source what the animation or video showed to the transcript alone, and do not render the frame.
- **The text layer can hold what the page hides.** A later build's bar or label may sit in an
  earlier slide's text layer, invisible (lecture 10's slide 39). Text-layer checks confirm wording
  and values; whether something is visible needs a render.
- Place images with `embed_slide_images.py` (with `--deck-label` for multi-deck lectures), once per
  wiki page that cites the slides, then hand-write captions for the figures where the caption
  should say what to look at. The script anchors each image after the block holding the
  **first** citation of that slide, and a range spanning up to 12 slides counts for every slide in
  it ("slides 96–99" counts for 99), so keep such ranges out of overview paragraphs or the image
  lands in the introduction. A longer range still anchors its first slide (lecture 12's "slides
  94–111" put slide 94 in the coverage paragraph), and the page's opening source line counts as
  overview ("slides 114–117 are PDF pages 112–115"). A citation of another lecture's slides ("lecture 8's slides 100–109") anchors
  too, on this lecture's slides of the same numbers; list where every image landed after the run. A block ending "(slide N):" before a display formula, a table or a
  code block gets the image between the sentence and what it introduces; move it below. On topic pages, cite "lecture N, slide M" and
  embed with `--deck-label "Lecture N"` so captions name the lecture. The script embeds every
  cited slide that has an image, so a topic-page table of slide ranges collects dozens: link the
  lecture page's sections from such a table, and cite directly the slides whose figure belongs.
- **Never type an image path.** `--format auto` makes some renders `.png`; a hand-placed image
  takes its path from the slide file (lecture 10: fourteen guessed `.jpg` links were wrong).
- Each slide file's header lists which of its slides have images and why the others do not.
  `grep -o 'raw/images/[^)]*' wiki/NN-*.md` enumerates a lecture's wiki images. There is no
  image index file.
- The chat resolves a relative image path by reading it; `INDEX.md` tells it never to construct
  one. Attribution for every rendered slide is in `LICENSE.md`.

| Lecture | Files | Where they came from |
| --- | --- | --- |
| 1 Introduction (parts 1 and 2) | 64 of 119 pages | 47 from `lecture_1_part_1.pdf` (69 pages), 17 from `lecture_1_part_2.pdf` (50 pages) |
| 2 Image Classification with Linear Classifiers | 41 of 102 pages | `lecture_2.pdf` (102 pages, printed 1–104) |
| 3 Regularization and Optimization | 24 of 119 pages | `lecture_3.pdf` (119 pages, printed 1–123) |
| 4 Neural Networks and Backpropagation | 35 of 147 pages | `lecture_4.pdf` (147 pages, printed 1–152) |
| 5 Image Classification with CNNs | 53 of 141 pages | `lecture_5.pdf` (141 pages, printed 1–141) |
| 6 Training CNNs and CNN Architectures | 33 of 97 pages | `lecture_6.pdf` (97 pages, printed 1–97) |
| 7 Recurrent Neural Networks | 43 of 124 pages | `lecture_7.pdf` (124 pages, printed 1–133) |
| 8 Attention and Transformers | 23 of 122 pages | `lecture_8.pdf` (122 pages, printed 1–122) |
| 9 Detection, Segmentation, Visualization, and Understanding | 53 of 178 pages | `lecture_9.pdf` (178 pages, printed 1–178) |
| 10 Video Understanding | 47 of 103 pages | `lecture_10.pdf` (103 pages, printed 1–103) |
| 11 Large-Scale Distributed Training | 30 of 148 pages | `lecture_11.pdf` (148 pages, printed 1–148) |
| 12 Self-Supervised Learning | 60 of 115 pages | `lecture_12.pdf` (115 pages, printed 1–117) |

## Rebuilding

Built and updated by the `cairn-kb` skill. To add newly released lectures,
append entries to `TODO.md` and re-run the skill — it only does unchecked work.
When a run is committed and pushed, move its `TODO.md` section verbatim to
`BUILD_LOG.md`, so `TODO.md` keeps only open work. Add here only a lesson
that applies to every lecture, stated in general form.
