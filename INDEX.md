# CS231N — Deep Learning for Computer Vision (Stanford, Spring 2025)

Stanford's CS231N teaches computer vision through deep learning: image classification with
linear classifiers and neural networks, convolutional networks and their architectures,
recurrent networks and transformers, detection, segmentation and video, large-scale training,
self-supervised learning, generative models, 3D vision, vision and language, robot learning,
and human-centred AI. The Spring 2025 offering is taught by Fei-Fei Li and Ehsan Adeli, with Zane
Durante and guest lecturers; the course website is <https://cs231n.stanford.edu/2025/>.

> **Coverage: 2 of 18 lectures.** This knowledge base currently covers **Lecture 1
> (Introduction) and Lecture 2 (Image Classification with Linear Classifiers) only**. It has
> nothing on lectures 3–18 — regularization and optimization, backpropagation, CNNs and everything
> after. For a question about a later topic, say that this KB does not cover it yet rather than
> answering as if from the course; the
> [course roadmap](wiki/course-logistics.md#course-roadmap) shows which lecture a topic belongs
> to, and [SEE_ALSO.md](SEE_ALSO.md) lists sibling knowledge bases that cover some of that
> material.

## How to read this knowledge base

- **Start with the wiki.** Each lecture has a page in `wiki/` written to stand alone, citing the
  transcript and slides it came from. Topic pages gather what the course says about one concept.
- **Citations.** "(≈24:10)" is a timestamp in the lecture video and in the transcript. Slide
  numbers are the numbers printed on the slides, which are not always the PDF page numbers.
  Lecture 1 has **two slide decks, each numbered from 1**, so its slides are cited "part 1,
  slide N" (Fei-Fei Li's history) or "part 2, slide N" (Ehsan Adeli's course overview); part 2
  is missing printed numbers 4, 5 and 45, so part 2, slide 53 is PDF page 50. Lecture 2 has one
  deck, cited "slide N" on its own page and "lecture 2, slide N" on topic pages; it is missing
  printed numbers 32 and 49, so slide 104 is PDF page 102.
- **Transcripts are edited.** `raw/transcripts/` holds copy-edited transcripts — punctuated,
  filler removed, mis-heard names and terms restored, every change listed in the file's header —
  with every `[M:SS]` marker in its original place. Read these, not the raw captions, which are
  not published here. Words the editor could not recover are marked `[unclear: …]` or `[Ed: …]`.
- **Slides are transcribed.** `raw/slides/` holds every slide's text, tables and a prose
  description of every figure. For numbers — table cells, chart values, grading percentages —
  quote the slide file, not a picture.
- **Some slides were never presented.** Lecture 2's recording skips the administrative slides
  (2–4) and ends at 1:06:37, before the multiclass SVM loss (a reading assignment, slides 85–100)
  and the softmax-vs-SVM comparison (slides 101–104). Those are sourced to the slides alone, and
  the deck's questions there have no printed answers: say so rather than presenting an answer as
  the course's.
- **Logistics come from slides only.** Lecture 1's logistics slides were not presented in the
  recording. Grading, late days, assignments and policies are in
  [course logistics](wiki/course-logistics.md), sourced to the part 2 slides as posted on
  April 1, 2025; the course website is authoritative for anything that changed later.

## Images

**Lectures 1 and 2 have slide images**: lecture 1 has 64 (47 from the part 1 deck, 17 from the
part 2 deck) and lecture 2 has 41. No other lecture has any yet. Each image sits under its `## Slide N` heading in `raw/slides/`, and
in the wiki passage that cites that slide.

- **Use an image path you have actually read in a file. Never construct one from the pattern,
  and never assume a slide has an image because a neighbouring one does.** Most slides have none.
  Each slide file's header lists exactly which of its slides have images.
- To show an image, read its path (e.g. `raw/images/01-introduction-part-1/slide-44.jpg`) and use
  the URL that comes back. Some images are `.png`, not `.jpg`; use the path exactly as written.
- Prefer the transcription for numbers. Show one image at a time, where it helps more than words,
  and keep its slide citation.

## Contents

### Lectures

- [Lecture 1 — Introduction](wiki/01-introduction.md) — Fei-Fei Li's history of computer vision
  and deep learning (the Cambrian explosion, Hubel and Wiesel, Roberts, Marr, the AI winter,
  Biederman and Thorpe, grouping, SIFT, Viola–Jones, the perceptron, XOR, the Neocognitron,
  backpropagation, LeNet, ImageNet, AlexNet, the deep-learning explosion, GPUs, bias and harm),
  then Ehsan Adeli's tour of the course's four parts and its learning objectives. 64 embedded
  slide images.

- [Lecture 2 — Image Classification with Linear Classifiers](wiki/02-image-classification.md) —
  Ehsan Adeli on the image classification task and the semantic gap; its challenges (viewpoint,
  illumination, clutter, occlusion, deformation, intraclass variation, context); the data-driven
  approach; the nearest-neighbour and k-NN classifiers, L1 and L2 distance, decision regions;
  hyperparameters, validation sets and cross-validation; CIFAR-10; the linear classifier
  $f(x, W) = Wx + b$ and its algebraic, visual and geometric viewpoints; what it cannot separate;
  loss functions; the softmax classifier, cross-entropy and KL divergence; and, from the slides
  only, the multiclass SVM loss and softmax vs. SVM. 41 embedded slide images.

### Topics

- [ImageNet and the ImageNet challenge](wiki/imagenet.md) — why data was the missing ingredient;
  the dataset (15 million images, 22,000 categories); the challenge (1,000 classes, 1,431,167
  images); the winning error by year from 28.2 to 2.3, with the human figure; why AlexNet won in
  2012 (backpropagation plus data, on an architecture close to the Neocognitron's).
- [Computer vision tasks](wiki/computer-vision-tasks.md) — what each task asks for:
  classification, semantic segmentation, object detection, instance segmentation, video
  classification, multimodal video understanding, visualization, retrieval, pose, captioning,
  visual relationships, generation — and which lecture covers each.
- [Image classification](wiki/image-classification.md) — the task, the semantic gap, why it is
  hard, the data-driven approach (collect, train, predict), CIFAR-10, and how well pixel-based
  k-NN does (about 28–29% against 10% chance).
- [k-nearest neighbours](wiki/k-nearest-neighbors.md) — the algorithm and its NumPy code; L1 and
  L2 distance and when to prefer each; decision regions and ties; $O(1)$ training and $O(N)$
  prediction; why k-NN on pixels is never used.
- [Hyperparameters and validation](wiki/hyperparameters-and-validation.md) — what a hyperparameter
  is; why not to tune on the training or test set; validation sets; cross-validation and when deep
  learning skips it; "run on the test set once at the very end".
- [Linear classifiers](wiki/linear-classifiers.md) — $f(x, W) = Wx + b$ and its dimensions for
  CIFAR-10; the bias; algebraic, visual (templates) and geometric (hyperplanes) viewpoints; the
  cases it cannot separate; linear layers inside AlexNet and ResNet.
- [Loss functions](wiki/loss-functions.md) — the dataset loss as an average; the softmax loss with
  worked numbers, logits, maximum likelihood, KL divergence and cross-entropy, its value at
  initialisation ($\log C$); the multiclass SVM (hinge) loss and its worked example; softmax vs.
  SVM.
- [Course logistics](wiki/course-logistics.md) — the lecture-by-lecture roadmap and the course's
  four parts; lectures, sections, Ed, office hours; Assignment 1; grading weights (assignments
  45%, midterm 20%, project 35%); late days; the collaboration policy (including "do not submit
  AI-generated responses"); prerequisites; textbooks; learning objectives.

## Raw materials

- [`raw/transcripts/`](raw/transcripts/) — edited lecture transcripts with `[M:SS]` paragraph
  marks. Lecture 1: [01-introduction.md](raw/transcripts/01-introduction.md); lecture 2:
  [02-image-classification.md](raw/transcripts/02-image-classification.md).
- [`raw/slides/`](raw/slides/) — slide-by-slide transcriptions with section tables:
  [part 1](raw/slides/01-introduction-part-1.md) (69 slides) and
  [part 2](raw/slides/01-introduction-part-2.md) (50 pages, printed numbers 1–53) for lecture 1;
  [lecture 2](raw/slides/02-image-classification.md) (102 pages, printed numbers 1–104).
- [`sources.md`](sources.md) — every document the course website links, with its canonical URL.
  Slide PDFs are **not** committed here; link to them at those URLs.
- [`LICENSE.md`](LICENSE.md) — what may be reused, and the attribution of every rendered image.
- [`SEE_ALSO.md`](SEE_ALSO.md) — sibling knowledge bases for neighbouring courses.
