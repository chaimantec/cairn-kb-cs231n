# CS231N — Deep Learning for Computer Vision (Stanford, Spring 2025)

Stanford's CS231N teaches computer vision through deep learning: image classification with
linear classifiers and neural networks, convolutional networks and their architectures,
recurrent networks and transformers, detection, segmentation and video, large-scale training,
self-supervised learning, generative models, 3D vision, vision and language, robot learning,
and human-centred AI. The Spring 2025 offering is taught by Fei-Fei Li and Ehsan Adeli, with Zane
Durante and guest lecturers; the course website is <https://cs231n.stanford.edu/2025/>.

> **Coverage: 4 of 18 lectures.** This knowledge base currently covers **Lecture 1
> (Introduction), Lecture 2 (Image Classification with Linear Classifiers), Lecture 3
> (Regularization and Optimization) and Lecture 4 (Neural Networks and Backpropagation) only**. It
> has nothing on lectures 5–18 — convolutional networks and everything after. For a question about a later topic, say that this KB does not cover it yet rather than
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
  printed numbers 32 and 49, so slide 104 is PDF page 102. Lecture 3 has one deck, cited the same
  way ("lecture 3, slide N" on topic pages); it is missing printed numbers 10, 11, 12 and 29, so
  slide 123 is PDF page 119. Lecture 4 has one deck, cited the same way ("lecture 4, slide N" on
  topic pages); it is missing printed numbers 2, 47, 112, 113 and 114, so slide 152 is PDF page
  147.
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
  the course's. Lecture 3's recording skips its administrative slides (2–4) and ends at 1:08:25 in
  the look ahead to neural networks; slides 100–101 and the deck's appendix of "Slides from
  Previous Years" (slides 102–123: Nesterov momentum, AdaGrad, L-BFGS, softmax vs. SVM, whether a
  zero-loss W is unique) are sourced to the slides alone. Lecture 4's recording skips its
  administrative slides (3–4) and the "Today: Deep Learning" examples (slides 12–21: DALL-E,
  GPT-4, Segment Anything, Sora), which are described from the slides alone; it covers everything
  else, the matrix-multiply example (slides 143–150) only in outline.
- **Printed slips are flagged, not corrected.** Where a deck's worked example prints a wrong
  number or sign, the slide file keeps it as printed with an `[Ed: …]` line and the wiki page says
  so. Quote the correction, not the slip. Lecture 4's matrix-multiply example (slides 143–150)
  prints an output y that is not the product of its x and w.
- **Lecture 3's optimizer-comparison animations are not in the PDF.** Its slides comparing
  optimizers' paths on a loss surface show only the surface and a legend, as does lecture 4's
  recap of them (slide 10). What the paths did is
  known only from the lecturer's spoken description; do not describe them from the slides.
- **Logistics come from slides only.** Lecture 1's logistics slides were not presented in the
  recording. Grading, late days, assignments and policies are in
  [course logistics](wiki/course-logistics.md), sourced to the part 2 slides as posted on
  April 1, 2025; the course website is authoritative for anything that changed later.

## Images

**Lectures 1–4 have slide images**: lecture 1 has 64 (47 from the part 1 deck, 17 from the
part 2 deck), lecture 2 has 41, lecture 3 has 24 and lecture 4 has 35. No other lecture has any
yet. Each image sits under its `## Slide N` heading in `raw/slides/`, and
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

- [Lecture 3 — Regularization and Optimization](wiki/03-regularization-optimization.md) — Zane
  Durante on the regularized loss $L(W)$ plus $\lambda R(W)$; prefer simpler models and Occam's
  razor; L2, L1 and elastic net and which weights each prefers; why regularize; the loss
  landscape; random search; numerical vs. analytic gradients and the gradient check; gradient
  descent and minibatch SGD; poor conditioning, local minima, saddle points and noisy gradients;
  SGD with momentum, RMSProp, Adam with bias correction, AdamW and weight decay; learning rates,
  step, cosine, linear and inverse-sqrt decay, warm-up and the batch-size rule of thumb;
  second-order methods and the Newton step; defaults in practice; a preview of two-layer networks;
  and, from the slides only, Nesterov momentum, AdaGrad and L-BFGS. 24 embedded slide images.

- [Lecture 4 — Neural Networks and Backpropagation](wiki/04-neural-networks-backpropagation.md) —
  Ehsan Adeli on the 2- and 3-layer network $f = W_2 \max(0, W_1 x)$; why non-linearity (polar
  coordinates) and why the max matters; hidden units as 100 shared templates; activation functions
  (ReLU, Leaky ReLU, ELU, GELU, SiLU, sigmoid, tanh) and how to choose; how layers are counted;
  a 2-layer network trained in 20 lines of NumPy; network size, capacity and "use stronger
  regularization instead"; biological neurons and the limits of the analogy; computational graphs;
  backpropagation worked on $f = (x+y)z$ and on a sigmoid neuron; upstream, local and downstream
  gradients; add, mul, copy and max gates; flat code and PyTorch's forward/backward API; Jacobians,
  the elementwise ReLU example and the matrix-multiply gradients; and, from the slides only, the
  DALL-E, GPT-4, Segment Anything and Sora examples. 35 embedded slide images.

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
  learning skips it; "run on the test set once at the very end"; lecture 3's regularization
  strength and learning rate; lecture 4's network size and activation function.
- [Linear classifiers](wiki/linear-classifiers.md) — $f(x, W) = Wx + b$ and its dimensions for
  CIFAR-10; the bias; algebraic, visual (templates) and geometric (hyperplanes) viewpoints; the
  cases it cannot separate; linear layers inside AlexNet and ResNet.
- [Loss functions](wiki/loss-functions.md) — the dataset loss as an average; the softmax loss with
  worked numbers, logits, maximum likelihood, KL divergence and cross-entropy, its value at
  initialisation ($\log C$); the multiclass SVM (hinge) loss and its worked example; softmax vs.
  SVM.
- [Regularization](wiki/regularization.md) — the regularized loss and the strength $\lambda$;
  prefer simpler models; L2, L1 and elastic net, with the worked example of which weights each
  prefers; why regularize; L2 inside Adam vs. weight decay in AdamW; tuning $\lambda$ rather than a
  network's size.
- [Neural networks](wiki/neural-networks.md) — fully connected networks (MLPs) built from the
  linear classifier; their dimensions; why they need a non-linearity; hidden units as templates;
  the activation functions and how to choose one; how layers are counted; size, capacity and
  regularization; the brain analogy and its limits.
- [Backpropagation and computational graphs](wiki/backpropagation.md) — why gradients are not
  derived by hand; computational graphs; upstream × local = downstream at each node; the two worked
  examples; the sigmoid gate; add, mul, copy and max gate patterns; flat and modular (PyTorch)
  implementations; gradients and Jacobians for vectors; never forming the Jacobian (ReLU); the
  matrix-multiply gradients.
- [Gradient descent and SGD](wiki/gradient-descent.md) — the loss landscape; the gradient,
  numerical vs. analytic, and the gradient check; gradient descent, stopping, minibatch SGD and
  epochs; poor conditioning (condition number), local minima, saddle points, noisy gradients;
  first- vs. second-order methods, the Newton update and why deep learning avoids it.
- [Optimizers](wiki/optimizers.md) — SGD with momentum (both formulations), Nesterov momentum,
  AdaGrad, RMSProp, Adam and its bias correction and default settings, AdamW; which to use.
- [Learning rates and schedules](wiki/learning-rate-schedules.md) — what too high and too low look
  like; step, cosine, linear and inverse-square-root decay with their formulas; linear warm-up;
  scaling the learning rate with the batch size.
- [Course logistics](wiki/course-logistics.md) — the lecture-by-lecture roadmap and the course's
  four parts; lectures, sections, Ed, office hours; Assignment 1; grading weights (assignments
  45%, midterm 20%, project 35%); late days; the collaboration policy (including "do not submit
  AI-generated responses"); prerequisites; textbooks; learning objectives.

## Raw materials

- [`raw/transcripts/`](raw/transcripts/) — edited lecture transcripts with `[M:SS]` paragraph
  marks. Lecture 1: [01-introduction.md](raw/transcripts/01-introduction.md); lecture 2:
  [02-image-classification.md](raw/transcripts/02-image-classification.md); lecture 3:
  [03-regularization-optimization.md](raw/transcripts/03-regularization-optimization.md); lecture 4:
  [04-neural-networks-backpropagation.md](raw/transcripts/04-neural-networks-backpropagation.md).
- [`raw/slides/`](raw/slides/) — slide-by-slide transcriptions with section tables:
  [part 1](raw/slides/01-introduction-part-1.md) (69 slides) and
  [part 2](raw/slides/01-introduction-part-2.md) (50 pages, printed numbers 1–53) for lecture 1;
  [lecture 2](raw/slides/02-image-classification.md) (102 pages, printed numbers 1–104);
  [lecture 3](raw/slides/03-regularization-optimization.md) (119 pages, printed numbers 1–123);
  [lecture 4](raw/slides/04-neural-networks-backpropagation.md) (147 pages, printed numbers 1–152).
- [`sources.md`](sources.md) — every document the course website links, with its canonical URL.
  Slide PDFs are **not** committed here; link to them at those URLs.
- [`LICENSE.md`](LICENSE.md) — what may be reused, and the attribution of every rendered image.
- [`SEE_ALSO.md`](SEE_ALSO.md) — sibling knowledge bases for neighbouring courses.
