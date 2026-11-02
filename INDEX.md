# CS231N — Deep Learning for Computer Vision (Stanford, Spring 2025)

Stanford's CS231N teaches computer vision through deep learning: image classification with
linear classifiers and neural networks, convolutional networks and their architectures,
recurrent networks and transformers, detection, segmentation and video, large-scale training,
self-supervised learning, generative models, 3D vision, vision and language, robot learning,
and human-centred AI. The Spring 2025 offering is taught by Fei-Fei Li and Ehsan Adeli, with Zane
Durante and guest lecturers; the course website is <https://cs231n.stanford.edu/2025/>.

> **Coverage: 11 of 18 lectures.** This knowledge base currently covers **Lecture 1
> (Introduction), Lecture 2 (Image Classification with Linear Classifiers), Lecture 3
> (Regularization and Optimization), Lecture 4 (Neural Networks and Backpropagation), Lecture 5
> (Image Classification with CNNs), Lecture 6 (Training CNNs and CNN Architectures), Lecture 7
> (Recurrent Neural Networks), Lecture 8 (Attention and Transformers), Lecture 9 (Detection,
> Segmentation, Visualization, and Understanding), Lecture 10 (Video Understanding) and Lecture 11
> (Large-Scale Distributed Training) only**. It has nothing on lectures 12–18 — self-supervised
> learning and everything after. For a question about a later topic, say that this KB does not cover it yet rather than
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
  147. Lecture 5 has one deck, cited the same way ("lecture 5, slide N" on topic pages), and its
  141 printed numbers match its PDF pages exactly; so do lecture 6's 97 ("lecture 6, slide N" on
  topic pages). Lecture 7 has one deck ("lecture 7, slide N" on topic pages); it is missing printed
  numbers 19, 20, 52, 53, 71, 72, 73, 100 and 103, and its page 118 prints no number (it is slide
  127), so slide 133 is PDF page 124. Lecture 8 has one deck ("lecture 8, slide N" on topic pages),
  and its 122 printed numbers match its PDF pages exactly; so do lecture 9's 178 ("lecture 9, slide
  N" on topic pages) and lecture 10's 103 ("lecture 10, slide N" on topic pages; ten of its pages,
  mostly video stills, print no number, and their labels follow from their neighbours), and lecture
  11's 148 ("lecture 11, slide N" on topic pages).
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
  else, the matrix-multiply example (slides 143–150) only in outline. Lecture 5's recording skips
  its administrative slides (2–3) and its appendix of "Slides from Previous Years" (slides
  109–141: older convolution and pooling summaries, 1x1 convolutions, the ConvNetJS demo and a
  history from the Mark I Perceptron to the Neocognitron), which are sourced to the slides alone.
  Lecture 6's recording skips only its course-logistics slide (2); it adds spoken answers on LoRA
  and on ResNet's paired convolutions that no slide shows. Lecture 7's recording also skips only its
  course-logistics slide (2); its spoken answers go beyond the slides on chunked backpropagation,
  embedding layers, start tokens, and greedy decoding, sampling and beam search, and the colour code
  of its interpretable-cell figures (red for $-1$, blue for $1$) is spoken, not printed. Lecture 8's
  recording skips its administrative slide (2) and leaves four parts of the deck to the slides
  alone: the matrix-shape and memory slides (68–78, summarised in a sentence), the GPT-2 and GPT-3
  sizes (94–95), transformer language models (96–99, one sentence) and "Tweaking Transformers"
  (110–120: pre-norm, RMSNorm, SwiGLU, mixture of experts), left "as extra reading". Its spoken
  additions include the attention paper's ICLR 2025 award, a search-engine analogy for keys and
  values, a remark on "decoder-only attention", and arguments for parallelism and for attention's
  quadratic cost. Lecture 9's recording skips its administrative slide (2) and the deck's
  "Additional Reading Material" (slides 150–178: convolution and transposed convolution as matrix
  multiplication, RoI Pool and RoI Align, the R-CNN timing charts, Faster R-CNN's four losses and
  two stages, detection trade-offs, guided backpropagation), which are sourced to the slides alone.
  It does walk through lecture 8's "Tweaking Transformers" slides, repeated as its slides 20–29.
  Its spoken additions include the per-pixel softmax loss for segmentation, a long run of answers
  about DETR's object queries, and the lecturer's views that the R-CNN family is "not being used
  anymore", that DETR is "deprecated", and that U-Net still leads in medical segmentation.
  Lecture 10 is a guest lecture by Ruohan Gao. Its recording covers the whole deck except the last
  slide ("Next time"), but the McGurk slides (89–91) are never mentioned, the "Apply Eye Makeup"
  visualization (82–83) is not spoken, and several slides are video stills whose video the PDF does
  not hold (the point-light display of slide 43 is known only from the lecturer's description).
  Its toy size-and-receptive-field tables (24–31) and C3D cost table (41) are walked through in
  words; the values are on the slides. Spoken additions include frame sampling for single-frame
  models, why Sports-1M is unstable (a list of YouTube URLs, many since deleted), C3D trained at
  Facebook, and the lecturer's hypothesis that the motion stream overfits less.
  Lecture 11's lecturer is not named in the recording or on the deck. Its recording skips the
  administrative slide (2: the midterm review session on Friday 5/9 and the in-class midterm on
  Tuesday 5/13) and does not reach the last ("Next time"). It walks through the GPU hardware,
  data parallelism, FSDP, HSDP, activation checkpointing and MFU in detail, then says the remaining
  slides "can check it offline" and gives context, pipeline and tensor parallelism a brief tour, so
  their details come from the slides. Its spoken additions include binning as the reason an H100
  enables 132 of its 144 SMs, a model left in 32-bit running about 20 times slower, how long big
  training runs last, rack and cluster sizes and cooling, asynchronous SGD, PyTorch's
  DistributedDataParallel, and MFU above 50% on A100s.
- **Printed slips are flagged, not corrected.** Where a deck's worked example prints a wrong
  number or sign, the slide file keeps it as printed with an `[Ed: …]` line and the wiki page says
  so. Quote the correction, not the slip. Lecture 4's matrix-multiply example (slides 143–150)
  prints an output y that is not the product of its x and w. Lecture 5's deck has four: slide 6's
  ship score omits the bias (as lecture 2's does), slide 101 swaps its two cube labels (the input
  is 64 x 224 x 224, the output 64 x 112 x 112), slide 124 says "Conv layer" under the pooling-summary
  heading, and slide 129 prints the softmax loss with minus signs in the exponents. Lecture 6's
  deck has four oddities, none in its arithmetic: slide 11's LayerNorm annotation says "per
  batch" although its N x 1 statistics are per sample; slide 35's VGG16 and VGG19 stacks draw 15
  and 17 weight layers, not 16 and 19; slide 57 labels ResNet's last stage "3x3 conv, 64" where
  slides 53–56 print 512; and slides 78–79 point to "Lecture 13" for visualization, which is
  lecture 9 in this offering. Lecture 7's deck has six: slide 65's character-sampling softmax is
  wrong in its first two columns (the scores give about (.04, .13, .00, .84) and
  (.25, .20, .06, .50), not the printed (.03, .84, .00, .13) and (.25, .20, .50, .05)), which the
  lecturer acknowledges; slide 66's matrix ends rows 2 and 3 in w14; slide 106 writes the input
  weights $W_{xh}$ and then $W_{hx}$; slide 110's chain has a lowercase $t$ where it means $T$;
  slide 116's gradient-clipping code computes the squared norm and calls it the norm; and slide 129
  repeats lecture 6's "3x3 conv, 64" label on ResNet's last stage. Lecture 8's deck has six: slide
  62's faded output line reads Y = AX for Y = AV (repeated on 63); the multi-head slides (66–78)
  keep the single-head scale $\sqrt{D_Q}$, where each head's query dimension is $D_H$; slide 77's
  "1.192 TB" of attention weights mixes units (at 2 bytes a weight it is 1,192 GiB, or 1.28 TB);
  slide 82 prints $O(N)$ memory for self-attention, which holds only with Flash Attention (slide
  78); slide 111 prints "identify function"; and slide 113's RMSNorm averages over N entries of a
  vector of shape D. Lecture 9's deck has six: slide 3's encoder labels its inputs x0, x1, x2, x2;
  slides 4, 21 and 23 repeat lecture 8's O(N) memory, "identify function" and RMSNorm slips;
  slide 43 labels the low-resolution stage "D3 x H/4 x W/4", the same size as the medium-resolution
  stages (repeated on 44 and 59); and slide 127 reprints lecture 2's ship score of 61.95, which
  omits the bias (with $b = -1.2$ it is 60.75). Lecture 10's deck has four: slide 30 prints the 3D
  CNN's pooled output as "24 x 1 x 1", a dimension short ($24 \times 1 \times 1 \times 1$);
  slides 35–37 label the 3D filter "Slide over x and y" although it also slides over time; slide
  41's column headed "MFLOPs" holds GFLOPs, and its three fully connected rows do not recompute
  from the layer sizes; and slide 75 says to copy the kernel $K_t$ times "in space", where the copies
  go along time. Lecture 11's deck has eight: slide 25's "1.875 PB" and slide 69's "63GB" are in
  binary units, and slide 69's Llama3-405B sequence length of 4096 differs from the 8192 of slides
  125 and 146; slides 46–64 are titled "FSPD"; slide 68 lists "Adam β1, β1"; slide 98's
  checkpointing counter prints a current memory of 2 with one box drawn, and slides 100–101 keep the
  counter while drawing all eight boxes; slide 112's 41% MFU does not follow from its 400 TFLOPs per
  GPU (40.4%); slide 138 says to shard the first layer "over row" and the second "over column", the
  opposite of its own drawing; and slides 139–143 label Z "[DxD]" where it is $N \times D$.
- **Lecture 3's optimizer-comparison animations are not in the PDF.** Its slides comparing
  optimizers' paths on a loss surface show only the surface and a legend, as do lecture 4's
  and lecture 5's recaps of them (lecture 4, slide 10; lecture 5, slide 8). What the paths did is
  known only from the lecturer's spoken description; do not describe them from the slides.
- **Logistics come from slides only.** Lecture 1's logistics slides were not presented in the
  recording. Grading, late days, assignments and policies are in
  [course logistics](wiki/course-logistics.md), sourced to the part 2 slides as posted on
  April 1, 2025; the course website is authoritative for anything that changed later.

## Images

**Lectures 1–11 have slide images**: lecture 1 has 64 (47 from the part 1 deck, 17 from the
part 2 deck), lecture 2 has 41, lecture 3 has 24, lecture 4 has 35, lecture 5 has 53, lecture 6
has 33, lecture 7 has 43, lecture 8 has 23, lecture 9 has 53, lecture 10 has 47 and lecture 11
has 30. No other
lecture has any yet. Each image sits under its `## Slide N` heading in `raw/slides/`, and
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

- [Lecture 5 — Image Classification with CNNs](wiki/05-image-classification-cnns.md) — Justin
  Johnson on the recap of lectures 2–4 (and Adam's ICLR 2025 Test of Time Award); hand-designed
  image features (colour histogram, HoG, bag of words) vs. end-to-end learning; why flattening an
  image destroys its spatial structure; ConvNets from LeCun et al. 1998 and AlexNet to the
  transformers that displaced them; the fully connected layer as template matching; the
  convolution layer (filters, activation maps, biases, batches, shapes) and the Q&A on it; why
  stacked convolutions need a non-linearity; what filters learn; output size, padding, receptive
  fields and stride; the worked example (a 10 x 32 x 32 output, 760 parameters, 768K multiply-adds);
  1D and 3D convolution; pooling and max pooling, with its Q&A; translation equivariance; and,
  from the slides only, the appendix (1x1 convolutions, the neuron view, the ConvNetJS demo, the
  history from the Mark I Perceptron to the Neocognitron). 53 embedded slide images.

- [Lecture 6 — Training CNNs and CNN Architectures](wiki/06-training-cnns-architectures.md) —
  Zane Durante on how to build CNNs and how to train them: normalization layers (LayerNorm; batch,
  layer, instance and group norm); dropout, why it works and test-time scaling; activation
  functions (sigmoid's vanishing gradients, ReLU, GELU, SiLU, where they go); the ImageNet winners'
  error and depth; VGG's $3 \times 3$ filters (a $7 \times 7$ receptive field, $27C^2$ vs.
  $49C^2$ weights); ResNet (the plain-network degradation, residual blocks, the full architecture,
  18–152 layers); weight initialization (too small, too large, Kaiming); per-channel image
  normalization; data augmentation (flips, random resized crops, test-time augmentation, colour
  jitter, cutout); transfer learning (frozen features, finetuning, the four-case table, LoRA,
  model zoos); and the hyperparameter recipe with random vs. grid search. 33 embedded slide images.

- [Lecture 7 — Recurrent Neural Networks](wiki/07-recurrent-neural-networks.md) — Zane Durante's
  clarifications of lecture 6 (dropout's $p$ in libraries; LayerNorm does not fix bad
  initialization, a toy experiment); Weights and Biases; one-to-many, many-to-one and many-to-many
  sequence tasks; the RNN's hidden state and recurrence $h_t = f_W(h_{t-1}, x_t)$, unrolling, the
  vanilla (Elman) RNN with tanh; a hand-built RNN that detects repeated 1s; computational graphs,
  backpropagation through time and its truncated form; a character-level language model on "hello",
  sampling, greedy decoding and beam search, embedding layers; min-char-rnn and generated
  Shakespeare and C code; interpretable cells; RNN tradeoffs; image captioning with a CNN and an
  RNN, its failures and dataset bias; VQA, visual dialog, navigation; multilayer RNNs; vanishing and
  exploding gradients and gradient clipping; the LSTM's gates, cell state and gradient flow, and the
  ResNet parallel; RWKV, Mamba and state space models. 43 embedded slide images.
- [Lecture 8 — Attention and Transformers](wiki/08-attention-transformers.md) — sequence-to-sequence
  translation with RNNs and its context-vector bottleneck; attention in the decoder (alignment
  scores, softmax weights, a new context vector per step) and English–French attention heatmaps;
  the general attention layer (dot-product and scaled dot-product similarity, multiple queries,
  keys and values) and cross-attention; self-attention, fused QKV, permutation equivariance,
  positional encoding, masking and multiple heads; self-attention as four matrix multiplies, its
  $O(N^2)$ cost and Flash Attention; RNNs, convolution and self-attention compared; the Transformer
  block and its sizes (original, GPT-2, GPT-3); transformer language models; the Vision
  Transformer; pre-norm, RMSNorm, SwiGLU and mixture of experts (slides only). Six printed slips
  noted. 23 embedded slide images.
- [Lecture 9 — Detection, Segmentation, Visualization, and Understanding](wiki/09-detection-segmentation-visualization.md)
  — a recap of the Vision Transformer (class token or pooled outputs) and a walk through pre-norm,
  RMSNorm, SwiGLU and mixture of experts; semantic segmentation (sliding window, fully
  convolutional networks, the per-pixel loss, unpooling, max unpooling, transposed convolution,
  U-Net); object detection (classification plus localization and the multitask loss, region
  proposals, R-CNN, Fast R-CNN, RoI Pool and RoI Align, region proposal networks, Faster R-CNN,
  YOLO and single-stage detectors, DETR and its object queries); instance segmentation with Mask
  R-CNN; visualization (linear-classifier templates, first-layer filters, saliency maps, CAM,
  Grad-CAM, guided backpropagation, ViT attention maps). Six printed slips noted. 53 embedded
  slide images.
- [Lecture 10 — Video Understanding](wiki/10-video-understanding.md) — guest lecture by Ruohan
  Gao. Video as a 4D tensor; video classification as action recognition; why video is big, and
  training on short clips; the single-frame CNN baseline; late fusion (FC layers or pooling), early
  fusion and 3D CNNs, with a toy comparison of sizes and receptive fields; 3D convolution and
  temporal shift-invariance; Sports-1M and its results; C3D and its cost; optical flow and
  two-stream networks (UCF-101); CNN features into an LSTM and recurrent convolutional networks;
  the nonlocal block (spatio-temporal self-attention); I3D's inflated architectures and weights
  (Kinetics-400); video transformers; visualizing video models; temporal action localization and
  spatio-temporal detection; audio-visual source separation and video understanding; efficient
  video understanding; egocentric video; video with LLMs. Four printed slips noted. 47 embedded
  slide images.
- [Lecture 11 — Large-Scale Distributed Training](wiki/11-large-scale-distributed-training.md) —
  Llama3-405B as the running example; inside an NVIDIA H100 (HBM, L2 cache, streaming
  multiprocessors, FP32 cores, Tensor Cores and mixed precision); GPU throughput from the K40 to the
  B200; server, rack, pod and Meta's 24,576-GPU cluster; TPUs, AMD MI325X and Trainium2; four axes
  of parallelism; data parallelism and its all-reduce; FSDP's broadcast-compute-delete schedule;
  HSDP; activation memory and activation checkpointing (compute and memory of each strategy); a
  scaling recipe; hardware and model FLOPs utilization (HFU, MFU) with the MFU of GPT-3, Gopher,
  Megatron-Turing NLG, PaLM and Llama3-405B; context parallelism (ring attention, Ulysses);
  pipeline parallelism, the bubble and microbatches; tensor parallelism and the two-layer trick;
  ND parallelism and Llama3-405B's configurations. Eight printed slips noted. 30 embedded slide
  images.

### Topics

- [ImageNet and the ImageNet challenge](wiki/imagenet.md) — why data was the missing ingredient;
  the dataset (15 million images, 22,000 categories); the challenge (1,000 classes, 1,431,167
  images); the winning error by year from 28.2 to 2.3, with the human figure; why AlexNet won in
  2012 (backpropagation plus data, on an architecture close to the Neocognitron's); the winners'
  depth, from 8 layers to 152.
- [Computer vision tasks](wiki/computer-vision-tasks.md) — what each task asks for:
  classification, semantic segmentation, object detection, instance segmentation, video
  classification, multimodal video understanding, visualization, retrieval, pose, captioning,
  visual relationships, generation — and which lecture covers each, with links to lecture 9's
  segmentation, detection and visualization pages and lecture 10's video page; lecture 7's captioning, VQA,
  visual dialog and navigation are on the image captioning page.
- [Image classification](wiki/image-classification.md) — the task, the semantic gap, why it is
  hard, the data-driven approach (collect, train, predict), CIFAR-10, how well pixel-based
  k-NN does (about 28–29% against 10% chance), hand-designed features vs. end-to-end
  learning, and a frozen pretrained network as a learned feature extractor.
- [k-nearest neighbours](wiki/k-nearest-neighbors.md) — the algorithm and its NumPy code; L1 and
  L2 distance and when to prefer each; decision regions and ties; $O(1)$ training and $O(N)$
  prediction; why k-NN on pixels is never used; nearest neighbours in a CNN's feature space.
- [Hyperparameters and validation](wiki/hyperparameters-and-validation.md) — what a hyperparameter
  is; why not to tune on the training or test set; validation sets; cross-validation and when deep
  learning skips it; "run on the test set once at the very end"; lecture 3's regularization
  strength and learning rate; lecture 4's network size and activation function; lecture 5's
  convolution and pooling hyperparameters; lecture 6's seven-step recipe, accuracy curves
  (overfitting, underfitting) and random vs. grid search; tracking runs with Weights and Biases
  (lecture 7).
- [Linear classifiers](wiki/linear-classifiers.md) — $f(x, W) = Wx + b$ and its dimensions for
  CIFAR-10; the bias; algebraic, visual (templates) and geometric (hyperplanes) viewpoints; the
  cases it cannot separate; linear layers inside AlexNet and ResNet; the templates recalled as a
  visualization (lecture 9).
- [Loss functions](wiki/loss-functions.md) — the dataset loss as an average; the softmax loss with
  worked numbers, logits, maximum likelihood, KL divergence and cross-entropy, its value at
  initialisation ($\log C$); the multiclass SVM (hinge) loss and its worked example; softmax vs.
  SVM; softmax at every time step of a language model (lecture 7); softmax at every pixel and the
  multitask loss of detection (lecture 9).
- [Regularization](wiki/regularization.md) — the regularized loss and the strength $\lambda$;
  prefer simpler models; L2, L1 and elastic net, with the worked example of which weights each
  prefers; why regularize; L2 inside Adam vs. weight decay in AdamW; tuning $\lambda$ rather than a
  network's size; dropout (redundant representations, the ensemble view, test-time scaling, and
  lecture 7's note on what $p$ means in libraries); the train-with-randomness, test-on-average
  pattern it shares with data augmentation.
- [Neural networks](wiki/neural-networks.md) — fully connected networks (MLPs) built from the
  linear classifier; their dimensions; why they need a non-linearity; hidden units as templates;
  the activation functions and how to choose one, and why sigmoid gave way to ReLU, GELU and
  SiLU (lecture 6), and tanh in recurrent networks (lecture 7); how layers are counted; size, capacity and
  regularization; the brain analogy and its limits.
- [Backpropagation and computational graphs](wiki/backpropagation.md) — why gradients are not
  derived by hand; computational graphs; upstream × local = downstream at each node; the two worked
  examples; the sigmoid gate; add, mul, copy and max gate patterns; flat and modular (PyTorch)
  implementations; gradients and Jacobians for vectors; never forming the Jacobian (ReLU); the
  matrix-multiply gradients; backpropagation through time in recurrent networks (lecture 7); a link
  to gradients with respect to the pixels (saliency, Grad-CAM, lecture 9); storing or recomputing
  activations for the backward pass, activation checkpointing (lecture 11).
- [Convolutional networks](wiki/convolutional-networks.md) — why ConvNets (spatial structure,
  end-to-end learning); the convolution layer and its shapes; parameters vs. hyperparameters;
  non-linearity between convolutions; output size, padding and stride, with common settings;
  counting parameters and multiply-adds; receptive fields; 1D, 3D and 1x1 convolution; pooling;
  translation equivariance; what filters learn; history from Hubel and Wiesel to transformers;
  links on to lecture 6's architectures; convolution compared with recurrence and attention, and
  the ViT patch embedding as a strided convolution (lecture 8); fully convolutional networks and
  the transposed convolution (lecture 9); 3D convolution for video and temporal shift-invariance
  (lecture 10).
- [CNN architectures](wiki/cnn-architectures.md) — block diagrams; the ImageNet winners' error and
  number of layers by year; AlexNet; VGG (small filters, the receptive field of stacked $3 \times 3$
  layers, parameter counts); ResNet (why deeper plain networks do worse, residual blocks, the full
  architecture and its depths, its results); the LSTM's cell state as ResNet's parallel over time
  (lecture 7); C3D and I3D, VGG and Inception carried into 3D (lecture 10).
- [Normalization layers](wiki/normalization-layers.md) — normalize, then scale and shift with
  learned parameters; LayerNorm and its shapes; batch, layer, instance and group norm compared;
  normalization and initialization, with lecture 7's experiment (LayerNorm narrows but does not
  close the gap left by bad initialization); layer normalization in the Transformer block,
  pre-norm and RMSNorm (lecture 8), and lecture 9's spoken argument for pre-norm.
- [Weight initialization](wiki/weight-initialization.md) — activations that vanish (scale 0.01) or
  explode (0.05) through six ReLU layers; Kaiming / MSRA initialization, $\sqrt{2 / D_{\text{in}}}$;
  convolution layers; how to tell it is right; why normalization does not replace it (lecture 7).
- [Data preprocessing and augmentation](wiki/data-augmentation.md) — per-channel mean and std
  normalization; augmentation as regularization; flips, random crops and scales, colour jitter,
  cutout; choosing augmentations; test-time augmentation.
- [Transfer learning](wiki/transfer-learning.md) — why a pretrained network's features transfer
  (nearest neighbours in feature space); freeze and retrain the last layer, or finetune
  everything; the similar/different, little/lots-of-data table; dataset bias; LoRA; model zoos;
  a pretrained CNN as the image encoder for captioning (lecture 7); pretrained backbones in
  detectors (lecture 9); C3D as a video feature extractor and I3D's ImageNet initialization
  (lecture 10).
- [Gradient descent and SGD](wiki/gradient-descent.md) — the loss landscape; the gradient,
  numerical vs. analytic, and the gradient check; gradient descent, stopping, minibatch SGD and
  epochs; poor conditioning (condition number), local minima, saddle points, noisy gradients;
  first- vs. second-order methods, the Newton update and why deep learning avoids it; a link to
  minibatch SGD split across GPUs (lecture 11).
- [Optimizers](wiki/optimizers.md) — SGD with momentum (both formulations), Nesterov momentum,
  AdaGrad, RMSProp, Adam and its bias correction and default settings, AdamW; which to use; a
  link to Adam's state as per-weight memory in distributed training (lecture 11).
- [Learning rates and schedules](wiki/learning-rate-schedules.md) — what too high and too low look
  like; step, cosine, linear and inverse-square-root decay with their formulas; linear warm-up;
  scaling the learning rate with the batch size.
- [Recurrent neural networks](wiki/recurrent-neural-networks.md) — sequence tasks (one to many,
  many to one, many to many); the hidden state and the recurrence; the vanilla RNN; training by
  backpropagation through time, truncated; multilayer RNNs; why gradients vanish or explode, and
  gradient clipping; advantages and disadvantages; the sequence-to-sequence encoder and decoder and
  the context-vector bottleneck that attention removes (lecture 8); modern RNNs (state space
  models, RWKV, Mamba); CNN features into an LSTM, and recurrent convolutional networks, for video
  (lecture 10).
- [LSTM](wiki/lstm.md) — the LSTM's equations; the input, forget, output and "gate" gates and the
  cell state; the cell diagram; why gradients flow along the cell state; whether it solves vanishing
  gradients; the parallel with ResNet and Highway Networks.
- [Character-level language models](wiki/language-models.md) — training as per-step softmax
  classification on "hello"; sampling, greedy decoding and beam search (and slide 65's misprinted
  softmax); embedding layers; min-char-rnn; generated Shakespeare and C code; interpretable cells;
  transformer language models with masked self-attention (lecture 8); Llama3-405B as lecture 11's
  example of training a large language model at scale.
- [Image captioning and visual question answering](wiki/image-captioning.md) — a pretrained CNN's
  features fed into a captioning RNN; generation from start to end token; good captions and
  failures (hallucination, dataset bias); VQA's two formulations; visual dialog; visual language
  navigation; captioning as a use of cross-attention (lecture 8).
- [Attention](wiki/attention.md) — the sequence-to-sequence bottleneck and attention in the decoder
  (alignment scores, attention weights, context vectors); attention heatmaps in translation; the
  general attention layer (scaled dot-product similarity, multiple queries, keys and values) and a
  search-engine intuition; cross-attention and self-attention; permutation equivariance and
  positional encoding; masked and multi-headed self-attention; four matrix multiplies, $O(N^2)$
  cost and Flash Attention; attention compared with recurrence and convolution; DETR's
  cross-attention and ViT attention maps (lecture 9); the nonlocal block's space-time
  self-attention (lecture 10); splitting attention across GPUs with ring attention and Ulysses
  (lecture 11).
- [Transformers](wiki/transformers.md) — the Transformer block (self-attention, residual
  connections, layer normalization, per-vector MLP); stacks and their sizes (original, GPT-2,
  GPT-3); transformer language models; the Vision Transformer, with pooled outputs or a class
  token (lecture 9); pre-norm, RMSNorm, SwiGLU and mixture of experts, with lecture 9's spoken
  walk-through; why transformers took over; video transformers named (lecture 10); context and
  tensor parallelism for training transformers on many GPUs (lecture 11).
- [Image segmentation](wiki/image-segmentation.md) — semantic segmentation as per-pixel
  classification; sliding windows; fully convolutional networks with downsampling and upsampling;
  the per-pixel loss; unpooling, max unpooling and the transposed convolution; U-Net and its skip
  connections; instance segmentation with Mask R-CNN (lecture 9).
- [Object detection](wiki/object-detection.md) — one object as classification plus localization
  with a multitask loss; why many objects are harder; region proposals; R-CNN, Fast R-CNN (RoI
  Pool and RoI Align, the timing comparison) and Faster R-CNN with its region proposal network;
  single-stage detectors and YOLO; DETR and its object queries (lecture 9); temporal action
  localization and spatio-temporal detection (lecture 10).
- [Visualizing what networks learn](wiki/visualizing-networks.md) — linear-classifier templates;
  first-layer filters; saliency maps from gradients with respect to pixels; CAM and its equations;
  Grad-CAM; guided backpropagation; attention maps in Vision Transformers (lecture 9); video
  models' appearance and motion inputs, and 3D filters as clips (lecture 10).
- [Video understanding](wiki/video-understanding.md) — video as a 4D tensor and training on clips;
  where a network combines frames (single frame, late fusion, early fusion, 3D CNN) and temporal
  shift-invariance; C3D; optical flow and two-stream networks; longer time spans with RNNs,
  recurrent convolutional networks and the nonlocal block; I3D and video transformers; Sports-1M,
  UCF-101, Kinetics-400 and AVA; action localization, visualization, audio, efficiency (lecture 10).
- [Distributed training](wiki/distributed-training.md) — the GPU's Tensor Cores and the memory and
  bandwidth hierarchy from one GPU to a cluster; the four axes (batch, sequence, layers, model
  dimension) in one table: DP, FSDP, HSDP, CP, PP and TP, what each splits and communicates; why
  data parallelism runs out of memory; activation checkpointing's compute and memory; MFU against
  HFU; the scaling recipe and 4D parallelism (lecture 11).
- [Course logistics](wiki/course-logistics.md) — the lecture-by-lecture roadmap and the course's
  four parts; lectures, sections, Ed, office hours; Assignment 1; grading weights (assignments
  45%, midterm 20%, project 35%); late days; the collaboration policy (including "do not submit
  AI-generated responses"); prerequisites; textbooks; learning objectives; the midterm review and
  in-class midterm dates (lecture 11, slide 2).

## Raw materials

- [`raw/transcripts/`](raw/transcripts/) — edited lecture transcripts with `[M:SS]` paragraph
  marks. Lecture 1: [01-introduction.md](raw/transcripts/01-introduction.md); lecture 2:
  [02-image-classification.md](raw/transcripts/02-image-classification.md); lecture 3:
  [03-regularization-optimization.md](raw/transcripts/03-regularization-optimization.md); lecture 4:
  [04-neural-networks-backpropagation.md](raw/transcripts/04-neural-networks-backpropagation.md);
  lecture 5: [05-image-classification-cnns.md](raw/transcripts/05-image-classification-cnns.md); lecture 6:
  [06-training-cnns-architectures.md](raw/transcripts/06-training-cnns-architectures.md); lecture 7:
  [07-recurrent-neural-networks.md](raw/transcripts/07-recurrent-neural-networks.md); lecture 8:
  [08-attention-transformers.md](raw/transcripts/08-attention-transformers.md); lecture 9:
  [09-detection-segmentation-visualization.md](raw/transcripts/09-detection-segmentation-visualization.md);
  lecture 10: [10-video-understanding.md](raw/transcripts/10-video-understanding.md); lecture 11:
  [11-large-scale-distributed-training.md](raw/transcripts/11-large-scale-distributed-training.md).
- [`raw/slides/`](raw/slides/) — slide-by-slide transcriptions with section tables:
  [part 1](raw/slides/01-introduction-part-1.md) (69 slides) and
  [part 2](raw/slides/01-introduction-part-2.md) (50 pages, printed numbers 1–53) for lecture 1;
  [lecture 2](raw/slides/02-image-classification.md) (102 pages, printed numbers 1–104);
  [lecture 3](raw/slides/03-regularization-optimization.md) (119 pages, printed numbers 1–123);
  [lecture 4](raw/slides/04-neural-networks-backpropagation.md) (147 pages, printed numbers 1–152);
  [lecture 5](raw/slides/05-image-classification-cnns.md) (141 pages, printed numbers 1–141);
  [lecture 6](raw/slides/06-training-cnns-architectures.md) (97 pages, printed numbers 1–97);
  [lecture 7](raw/slides/07-recurrent-neural-networks.md) (124 pages, printed numbers 1–133);
  [lecture 8](raw/slides/08-attention-transformers.md) (122 pages, printed numbers 1–122);
  [lecture 9](raw/slides/09-detection-segmentation-visualization.md) (178 pages, printed numbers 1–178);
  [lecture 10](raw/slides/10-video-understanding.md) (103 pages, printed numbers 1–103);
  [lecture 11](raw/slides/11-large-scale-distributed-training.md) (148 pages, printed numbers 1–148).
- [`sources.md`](sources.md) — every document the course website links, with its canonical URL.
  Slide PDFs are **not** committed here; link to them at those URLs.
- [`LICENSE.md`](LICENSE.md) — what may be reused, and the attribution of every rendered image.
- [`SEE_ALSO.md`](SEE_ALSO.md) — sibling knowledge bases for neighbouring courses.
