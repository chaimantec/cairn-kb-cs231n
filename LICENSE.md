# Licence and copyright

This repository is a **study aid compiled from Stanford CS231N course material**. It is not a
work with a single owner, so it carries no single repository-wide licence. Three layers of
authorship sit here, with three different copyright positions. Read this before reusing
anything from it.

The short version: **the explanatory writing is yours to reuse with attribution; the course
material and the third-party images in the slides are not mine to give you.**

---

## Layer 1 — the compilation's own editorial work

Copyright (c) 2026 chaimantec.

Licensed under **Creative Commons Attribution 4.0 International** (`CC-BY-4.0`),
<https://creativecommons.org/licenses/by/4.0/>. You may share and adapt it, including
commercially, with attribution.

This covers only the material original to this compilation:

- `INDEX.md`, `AGENTS.md`, `BUILD_LOG.md`, `TODO.md`, `kb.json`, `sources.md`, this file;
- the original explanatory prose in `wiki/`: the explanations, the connective argument, the
  organisation of the material into pages, and the editorial judgements about what is worth
  recording.

It does **not** extend to the lecture content those pages describe, nor to any passage in
`wiki/` that quotes the lecturer or a slide. Those are quotations, marked as such, and belong to
Layer 2 or Layer 3.

### Not offered under CC BY 4.0, even though I wrote the words

`raw/transcripts/` and `raw/slides/` are derivative works. The copy-editing, the `[Ed:]` notes
and the figure descriptions are mine; the lecture being transcribed and the slides being
described are not. I cannot license the underlying expression, so these directories are not
offered under CC BY 4.0. Read them, cite them, and quote them as you would quote the lecture
itself, but do not treat them as freely relicensable text.

The verbatim auto-captions the transcripts were edited from are **deliberately not published
here**. They are a complete reproduction of the lecture with no editorial contribution, so they
stay on the build machine (`raw/transcripts/original/`, gitignored). Nothing is lost for
verification: they can be regenerated from the public video with the `cairn-kb` skill's
`fetch_transcript.py`, using the video id in each transcript's front matter.

---

## Layer 2 — Stanford CS231N course material

**No licence exists, and none is granted here.**

The lectures and slide decks are the work of Fei-Fei Li, Ehsan Adeli, Zane Durante, the
CS231N course staff and guest lecturers (lecture 10: Ruohan Gao) (Stanford University, Spring 2025). They are published through the course
website, <https://cs231n.stanford.edu/2025/>, with the lecture videos on YouTube.

As checked on 2026-11-01, no licence, copyright or reuse statement appears on the course
website's index, schedule or project pages, and none covering the decks as a whole is printed in
the Lecture 1, 2, 3, 6, 7, 8, 9 or 10 decks (lectures 2, 3, 6, 7, 8, 9 and 10 checked on 2026-11-02). Publicly downloadable is not the same as licensed. Absent an express grant
the default applies: copyright arises automatically, and no reuse rights pass to anyone.

The images in `raw/images/` and the material described in `raw/slides/` are reproduced here for
study and commentary, relying on fair use (17 U.S.C. § 107) rather than on any permission. Only
slides that carry a figure are rendered. Title slides, text-only slides, section dividers and
photographs of course staff are not. Every deck is linked at its canonical URL beside the
material drawn from it. **That reliance is mine and does not transfer to you.** Fair use is a
defence to infringement, not a licence. It can justify a particular use by a particular user for
a particular purpose, and gives me nothing to pass downstream. If you want to reuse Layer 2
material, make your own assessment or ask the course staff.

**Takedown.** If the instructors or any rights holder asks for an image or a transcription to be
removed, it will be deleted along with every link to it.

---

## Layer 3 — third-party images reproduced inside the decks

The CS231N decks reproduce many images that are not Stanford's: photographs, historical figures,
figures from research papers, screenshots and charts. The decks themselves print a credit line
for most of them — a Creative Commons licence, a public-domain note, or "Figures copyright …,
reproduced with permission". **A permission granted to the course does not pass to this
repository**, and nothing here relicenses any of these images. The attributions below are copied
from the credit lines, citations and captions printed on the slides. Where nothing on the slide
identifies the source, the entry says so.

Several slides carry "Slide inspiration: Justin Johnson" (or Andrej Karpathy): the slide's
design follows an earlier CS231n deck by that lecturer. That is a design credit, not an image
licence, and is not repeated below.

### Lecture 1 — Introduction, part 1 (history of computer vision)

Deck: [lecture_1_part_1.pdf](https://cs231n.stanford.edu/slides/2025/lecture_1_part_1.pdf).
Rendered: 47 slides, in `raw/images/01-introduction-part-1/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 8, 12 | No third-party content identified: the deck's own Venn diagram. |
| 14 | Three fossil and Cambrian-animal images, credited "licensed under CC-BY 2.5" (two) and "CC-BY 3.0" (one). Authors not named. |
| 15 | Four close-up photographs of animal and human eyes. Not credited. |
| 16 | Camera-obscura engravings credited to Gemma Frisius (1545), Leonardo da Vinci and an 18th-century encyclopedia, each marked "This work is in the public domain". |
| 17 | Twelve photographs of cameras, credited on the slide as CC0 / public domain, "free to use", "Image by Roger H Goun … CC BY 2.0", "Image by NASA … CC BY 2.0", "Image by Derek Keats … CC BY 2.0; changes made" and "CC-BY 2.0; changes made". |
| 19 | Diagram of Hubel and Wiesel's 1959 experiment; "Cat image by CNX OpenStax is licensed under CC BY 4.0; changes made". |
| 20 | Figures from Lawrence G. Roberts, *Machine Perception of Three-Dimensional Solids*, 1963. |
| 21 | Scan of MIT AI Group Vision Memo No. 100, Seymour Papert, 1966 (linked on the slide: <https://dspace.mit.edu/handle/1721.1/6125>). |
| 22 | Cover of David Marr's book *Vision* (printed "Copyrighted Material"); basketball photographs "CC0 1.0 public domain". |
| 23 | Figures after Brooks and Binford (generalized cylinders, 1979) and Fischler and Elschlager (pictorial structures, 1973). Not otherwise credited. |
| 24 | Razor photograph "CC0 1.0 public domain" and its edge map. |
| 27 | Photographs from I. Biederman, *Science*, 1972. |
| 29 | Figure from Thorpe, Fize and Marlot, *Nature*, 1996, with an uncredited photograph of an EEG subject. |
| 30 | Figures from Kanwisher et al., *J. Neuroscience*, 1997, and Epstein and Kanwisher, *Nature*, 1998. |
| 32 | Normalized-cuts segmentations (Shi and Malik, 1997); photographs credited "CC BY 3.0", "public domain" and "CC-BY 2.0; changes made". |
| 33 | Stop-sign photographs "public domain"; SIFT matching (Lowe, 1999). |
| 34 | Group photograph with face detections (Viola and Jones, 2001). Not credited. |
| 35 | Caltech 101 image mosaic; PASCAL example photographs "CC0 1.0 public domain". |
| 36 | Title block of Rumelhart, Hinton and Williams (1986); a perceptron diagram; a photograph of the Mark I Perceptron (Rosenblatt). The diagram and photograph are not credited. |
| 37 | Cover of Minsky and Papert, *Perceptrons* (MIT Press reissue). |
| 38 | Neocognitron diagram (Fukushima, 1980). |
| 39 | "Illustration of Rumelhart et al., 1986 by Lane McIntosh, copyright CS231n 2017". |
| 40 | Convolutional-network diagram from LeCun et al., 1998. |
| 41 | Deep-autoencoder figure (Hinton and Salakhutdinov, 2006). |
| 43, 44 | ImageNet logo and image mosaic (Deng et al., 2009; Russakovsky et al., *IJCV* 2015). The bar chart on slide 44 is the deck's own. |
| 46, 47 | AlexNet architecture figure (Krizhevsky, Sutskever and Hinton, 2012); slide 47 also repeats the Neocognitron diagram. |
| 48 | Charts of CVPR paper counts and of ML+AI arXiv papers per month. The chart sources are not printed beyond "(source)". |
| 49 | "Lion image by Swissfrog is licensed under CC BY 3.0"; "Figure copyright Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton, 2012. Reproduced with permission."; architecture figures from Szegedy et al. (GoogLeNet), Simonyan and Zisserman (VGG) and He et al. (ResNet). |
| 50 | "Figures copyright Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton, 2012. Reproduced with permission." |
| 51 | Detection results from Ren, He, Girshick and Sun (2015); scene-parsing result from Farabet et al. (2012; printed "Fabaret"). |
| 52 | Two-stream network diagram (Simonyan and Zisserman, 2014) and a 3-D convnet diagram. |
| 53 | Pose-estimation results (Toshev and Szegedy, 2014) and Atari figures (Guo et al., 2014). |
| 54 | "Levy et al, 2016 Figure reproduced with permission"; galaxy images "public domain by NASA, usage permitted by ESA/Hubble, public domain by NASA, and public domain"; whale photograph "by Christin Khan … public domain … U.S. NOAA". |
| 55 | Photographs "CC0 Public domain" (pixabay URLs on the slide); "Captions generated by Justin Johnson using Neuraltalk2". |
| 56 | Scene-graph figure from Krishna, Lu, Bernstein and Fei-Fei (ECCV 2016). |
| 57 | "Figures copyright Justin Johnson, 2015. Reproduced with permission." (DeepDream); "Stylized images copyright Justin Johnson, 2017; reproduced with permission"; the Van Gogh paintings and other sources marked public domain. |
| 59 | DALL·E-generated images from Ramesh et al. / OpenAI (2021, <https://openai.com/blog/dall-e/>). |
| 61 | Data-centre photograph and image mosaic. Not credited. |
| 62, 63 | No third-party images: the deck's own charts. |
| 64 | Charts credited "Source: The Gradient", "Source: Crunchbase, VentureSource, Sand Hill Econometrics" and "Source: Statista". |
| 66 | Gender-classifier accuracy table and portraits ("Example Credit: Timnit Gebru"); screenshots of a *Washington Post* article (URL on the slide) and of HireVue's interview software. |
| 67 | Elderly-care graphic with a Stanford logo. No third-party credit printed. |
| 68 | Photograph of children, credited only by a fedandfit.com image URL; photograph marked "copyright-free United States government work". |

Not rendered from this deck: the title (1), the anniversary collage and staff photographs (2–4),
the intermediate Venn builds (5–7, 9–11), agenda and divider slides (13, 18, 26, 65, 69), the
text-only AI-winter slide (25), the plain RSVP fixation frame (28), recap and build slides that
repeat a rendered figure (31, 42, 45, 60), and slide 58, a black rectangle where a video did
not render.

### Lecture 1 — Introduction, part 2 (course overview)

Deck: [lecture_1_part_2.pdf](https://cs231n.stanford.edu/slides/2025/lecture_1_part_2.pdf).
Rendered: 17 slides, in `raw/images/01-introduction-part-2/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 8, 9, 10 | "This image by Nikita is licensed under CC-BY 2.0" (the cat photograph); the plots and network diagram are the deck's own. |
| 14 | Photographs "CC0 public domain", with the deck's own segmentation and detection overlays. |
| 15 | Video frames and a dog photograph with a saliency map. Not credited. |
| 16 | "Illustration of LeCun et al. 1998 from CS231n 2017 Lecture 1". |
| 17 | No third-party content identified: RNN, LSTM and attention diagrams. |
| 18 | Data- and model-parallelism diagram. Not credited. |
| 22 | "Image Courtesy of Rohit Kundu". |
| 23 | Photograph of Hoover Tower and its style-transferred version. Not credited. |
| 24 | DALL-E 2 image, marked on the slide "This image is public domain". |
| 25 | Diffusion diagram linked to <https://learnopencv.com/image-generation-using-diffusion-models/>; emoji samples from the course's Assignment 3. |
| 26 | Figure after Yasunaga et al., 2022; CLIP diagram "derived from https://github.com/openai/CLIP". |
| 27 | Figures from Choy et al. (3D-R2N2, 2016), Zhou et al. (point-voxel diffusion, 2021) and Gkioxari et al. (Mesh R-CNN, ICCV 2019). |
| 28 | Video frames from Li et al. (BEHAVIOR-1K, 2022) and Mandlekar, Xu et al. (2020). |
| 34 | CVPR 2025 Nashville logo and skyline photograph (not credited); CVPR paper-statistics chart (source not printed). |
| 52 | k-nearest-neighbour and linear-classifier figures; "Plot created using Wolfram Cloud". |

Not rendered from this deck: the title (1), instructor and guest-lecturer photographs (2, 3),
agenda, divider and title-only slides (6, 11–13, 19–21, 29, 30, 35), the cat-only build (7),
photographs of award winners and the award ceremony (31–33), the schedule screenshot (37), whose
table is transcribed in full in `raw/slides/`, and the text-only logistics slides (36, 38–44,
46–51, 53).

### Lecture 2 — Image Classification with Linear Classifiers

Deck: [lecture_2.pdf](https://cs231n.stanford.edu/slides/2025/lecture_2.pdf).
Rendered: 41 slides, in `raw/images/02-image-classification/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 7, 8, 9 | "This image by Nikita is licensed under CC-BY 2.0" (the tabby cat); the pixel grid and camera icons are the deck's own. |
| 10, 11, 14 | Cat photographs, each credited "This image is CC0 1.0 public domain". |
| 12 | Two photographs "CC0 1.0 public domain"; "This image by jonsson is licensed under CC-BY 2.0". |
| 13 | "This image by Umberto Salvagnin is licensed under CC-BY 2.0" (two); "This image by sare bear is licensed under CC-BY 2.0"; "This image by Tom Thai is licensed under CC-BY 2.0". |
| 15 | Two photographs of an animal behind a fence; "Image source:" a LinkedIn post URL printed on the slide. |
| 16 | ImageNet logo built from a photo mosaic, credited "This image is CC0 1.0 public domain". |
| 18 | The CC-BY 2.0 cat (Nikita) and its edge map; credit line "John Canny, 'A Computational Approach to Edge Detection', IEEE TPAMI 1986". |
| 19, 44, 47 | CIFAR-10 image grids; slides 43–44 cite Alex Krizhevsky, "Learning Multiple Layers of Features from Tiny Images", Technical Report, 2009. |
| 22 | Five small training photographs and the cat photograph. Not credited on this slide. |
| 23, 31, 33, 41, 42, 55, 89, 94, 99, 101 | No third-party content beyond photographs credited elsewhere in the deck: the deck's own worked examples, diagrams and plots (slides 94 and 99 reuse the cat, car and frog photographs credited on slide 65). |
| 29, 30, 34, 35 | k-nearest-neighbour decision-region plots, not credited; slide 35 links the CS231n demo at <http://vision.stanford.edu/teaching/cs231n-demos/knn/>. |
| 45 | Cross-validation chart. Source not printed. |
| 48 | Portrait photograph and three edited copies; "Original image is CC0 public domain". |
| 56 | Photograph of toy blocks, "This image is CC0 1.0 public domain". |
| 57 | Architecture figures from Krizhevsky et al. 2012 (AlexNet) and He et al. 2015 (ResNet), cited on the slide. |
| 60, 62 | The deck's own matrix example; slide 62 adds learned CIFAR-10 templates and the CIFAR-10 grid. |
| 63 | "Plot created using Wolfram Cloud"; "Cat image by Nikita is licensed under CC-BY 2.0"; small CIFAR-10 images. |
| 64 | No third-party content identified: the deck's own region plots. |
| 65 | "Cat image by Nikita is licensed under CC-BY 2.0; Car image is CC0 1.0 public domain; Frog image is in the public domain". |
| 77, 80 | The cat photograph (credited on slides 7 and 65) with the deck's own softmax diagram. |
| 84 | Rainbow heat-map image. Not credited. |

Not rendered from this deck: the title (1), administrative, syllabus and agenda slides (2–6), code
slides (17, 21, 24–28, 100), section titles (20, 51, 70), text-only slides (36, 50, 85), build steps
whose final step is rendered (37–40, 43, 46, 52–54, 59, 61, 71–76, 78–79, 86–88, 90–93, 95–98), the
repeated CIFAR-10 grid (58), the score-table slides whose table is transcribed in full (66–69), and
formula and question slides transcribed exactly (81–83, 102–104).

### Lecture 3 — Regularization and Optimization

Deck: [lecture_3.pdf](https://cs231n.stanford.edu/slides/2025/lecture_3.pdf).
Rendered: 24 slides, in `raw/images/03-regularization-optimization/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 35 | The alpine-valley photograph and the walking-man figure; slide 35 prints no credit, but the same images are credited on slide 31 ("This image is CC0 1.0 public domain") and slide 32 ("Walking man image is CC0 1.0 public domain"). |
| 46 | Two painted portraits, each credited "This image is in the public domain"; the slide does not name the sitters. |
| 59 | 3D saddle-surface plot; "Image source: https://en.wikipedia.org/wiki/Saddle_point". |
| 80 | Chart of ImageNet accuracy for weight decay vs. L2; "Source: https://www.fast.ai/posts/2018-07-02-adam-weight-decay.html". |
| 50, 51, 61 | Loss heat-maps (and, on 61, the deck's own curves and contour plot). Source not printed. |
| 83, 84, 86 | Loss-curve charts. Source not printed. |
| 85, 87, 88, 89 | Learning-rate plots. The slides cite papers for the schedules (Loshchilov and Hutter 2017, Radford et al. 2018, Feichtenhofer et al. 2018, Child et al. 2019; Devlin et al. 2018; Vaswani et al. 2017; Goyal et al. 2017), not as sources of the plots. |
| 122 | Cat, car and frog photographs; not credited in this deck (lecture 2's deck credits them on its slide 65). |
| 18, 28, 55, 57, 91, 92, 99, 104, 119 | No third-party content identifiable: the deck's own plots, diagrams and worked examples (slide 57's figure accompanies slide 58's citation of Dauphin et al. 2014; slide 104's, citations of Nesterov 1983 and 2004 and Sutskever et al. 2013). |

Not rendered from this deck: the title (1), administrative slides (2–4), section dividers (5, 30,
102), recaps of lecture 2 figures (6–9; slide 6 credits the cat "by Nikita" under CC-BY 2.0 and
slide 7 carries CC0 and CC-BY 2.0 credits for its photographs), tables, formulas, vectors and code
transcribed exactly, text slides, build steps whose last step is rendered (16–17, 27, 31–32,
53–54, 56, 58, 82, 90, 98, 103), heat-map frames whose animated paths are not in the PDF (60, 70,
75, 109), and the AdaGrad slides repeating slide 53's contour plot (111–114). The slide file's
header lists every slide and the reason.

### Lecture 4 — Neural Networks and Backpropagation

Deck: [lecture_4.pdf](https://cs231n.stanford.edu/slides/2025/lecture_4.pdf).
Rendered: 35 slides, in `raw/images/04-neural-networks-backpropagation/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 13 | Three DALL-E 2 images; "Image source: Sam Altman, https://openai.com/dall-e-2/, https://twitter.com/sama/status/1511724264629678084". |
| 14 | DALL-E 2 samples and architecture diagram; "Ramesh et al., Hierarchical Text-Conditional Image Generation with CLIP Latents, 2022." |
| 15, 16 | DALL-E 3 images and prompts; "Betker, James, et al. "Improving image generation with better captions." … https://cdn.openai.com/papers/dall-e-3.pdf (2023)." |
| 17 | Two GPT-4 conversation screenshots; "Image source: https://openai.com/research/gpt-4"; the taxi photograph inside one is marked "Source: Barnorama". |
| 18 | Segment Anything mask examples; "Kirillov et al., Segment Anything, 2023". |
| 19, 20, 21 | Sora video frames; "https://openai.com/research/video-generation-models-as-world-simulators" (on slide 19 the link is in the text layer, hidden under the image). |
| 41, 42 | Decision-region plots from a web demo; slide 42 cites "Web demo with ConvNetJS: http://cs.stanford.edu/people/karpathy/convnetjs/demo/classify2d.html" and the TensorFlow Playground. |
| 43 | Neuron illustration; "This image by Fotis Bobolas is licensed under CC-BY 2.0". |
| 46 | Neuron drawing; "This image by Felipe Perucho is licensed under CC-BY 3.0". |
| 48 | Neuron illustration; "This image is CC0 Public Domain". |
| 49 | The same CC0 illustration, and randomly wired network graphs from "Xie et al, "Exploring Randomly Wired Neural Networks for Image Recognition", IEEE/CVF International Conference on Computer Vision 2019". |
| 55 | Crop of the AlexNet architecture figure; "Figure copyright Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton, 2012. Reproduced with permission." |
| 56, 57 | Large computational-graph renderings; "Figure reproduced with permission from a Twitter post by Andrej Karpathy." |
| 116 | Screenshot of a file listing in the pytorch/pytorch GitHub repository. Source not printed. |
| 152 | The AlexNet architecture figure; no credit on this slide (slide 55 credits the same figure to Krizhevsky, Sutskever and Hinton, "Reproduced with permission"). |
| 26, 30, 33, 34, 54, 74, 80, 96, 100, 104, 105, 130, 137, 142, 150 | No third-party content identifiable: the deck's own plots, diagrams and worked examples (slide 30's strip is lecture 2's learned templates). |

Not rendered from this deck: the title (1), administrative slides (3–4), section dividers and
text, recaps of lecture 3 figures (6, 7, 11; slide 7 credits its landscape and walking-man images
as CC0 1.0 public domain), the optimizer animation frame (10), formulas, code and text transcribed
exactly (including the PyTorch source screenshots on 117–119), build steps whose last step is
rendered, and slide 35's repeat of slide 34's diagram. The slide file's header lists every slide
and the reason.

### Lecture 5 — Image Classification with CNNs

Deck: [lecture_5.pdf](https://cs231n.stanford.edu/slides/2025/lecture_5.pdf).
Rendered: 53 slides, in `raw/images/05-image-classification-cnns/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 18, 101 | Pooling diagram with an activation image downsampled from 224 to 112. Not credited. |
| 20, 21, 22, 25, 106 | Photograph of a red-eyed tree frog. Not credited on these slides (lecture 2 credits the same frog image as public domain). |
| 23 | Frog photograph and its histogram-of-oriented-gradients image; the slide cites Lowe (ICCV 1999) and Dalal and Triggs (CVPR 2005). |
| 24 | Cat and frog photographs, image patches and a codebook; the slide cites Fei-Fei and Perona (CVPR 2005). |
| 26, 34, 137 | AlexNet architecture figure; "Figure copyright Krizhevsky, Sutskever, and Hinton, 2012. Reproduced with permission." (slide 137: "Figures copyright Alex Krizhevsky, Ilya Sutskever, and Geoffrey Hinton, 2012. Reproduced with permission.", with AlexNet's learned filters). Slide 34 also shows the ImageNet logo mosaic; slide 26 an uncredited cat photograph. |
| 31 | "Illustration of LeCun et al. 1998 from CS231n 2017 Lecture 1". |
| 35 | "Figures copyright Shaoqing Ren, Kaiming He, Ross Girschick, Jian Sun, 2015. Reproduced with permission." and "Figures copyright Clement Farabet, 2012. Reproduced with permission." |
| 36 | "All images are CC0 Public domain" (six pixabay URLs printed on the slide); "Captions generated by Justin Johnson using Neuraltalk2". |
| 37 | Generated images from Rombach et al., "High-Resolution Image Synthesis with Latent Diffusion Models", CVPR 2022. No further credit. |
| 38 | Screenshot of the CS231n in-browser ConvNet demo. |
| 41 | Transformer diagram from Vaswani et al., "Attention is all you need", NeurIPS 2017; Vision Transformer diagrams from Dosovitskiy et al., "An Image is Worth 16x16 Words", ICLR 2021. |
| 68 | AlexNet's first-layer filters ("AlexNet: 64 filters, each 3x11x11"). Not otherwise credited. |
| 69 | "Visualization from [Springenberg et al, ICLR 2015]". |
| 108 | Four architecture figures, not credited on the slide: the LeCun et al. 1998 illustration of slide 31, the AlexNet figure of slide 34, a module diagram and a deep-network diagram. |
| 117 | Neuron-model diagram and a brain-surface image. Not credited. |
| 120 | Car photograph and its activation maps. Not credited. |
| 127 | Screenshots of the ConvNetJS CIFAR-10 demo, <http://cs.stanford.edu/people/karpathy/convnetjs/demo/cifar10.html>. |
| 133 | Mark I Perceptron photograph: "This image by Rocky Acosta is licensed under CC-BY 3.0". |
| 134 | "These figures are reproduced from Widrow 1960, Stanford Electronics Laboratories Technical Report with permission from Stanford University Special Collections." |
| 135 | "Illustration of Rumelhart et al., 1986 by Lane McIntosh, copyright CS231n 2017". |
| 136 | "Illustration of Hinton and Salakhutdinov 2006 by Lane McIntosh, copyright CS231n 2017". |
| 137 | Also "Illustration of Dahl et al. 2012 by Lane McIntosh, copyright CS231n 2017". |
| 138 | "Cat image by CNX OpenStax is licensed under CC BY 4.0; changes made". |
| 139 | "Retinotopy images courtesy of Jesse Gomez in the Stanford Vision & Perception Neuroscience Lab." |
| 140 | "Illustration of hierarchical organization in early visual pathways by Lane McIntosh, copyright CS231n 2017". |
| 141 | Neocognitron diagram ("Neocognitron [Fukushima 1980]"). Not otherwise credited. |
| 28, 47, 50, 51, 55, 57, 60, 61, 62, 65, 67, 75, 79, 80, 81, 87, 97, 98, 102, 114, 118 | No third-party content identifiable: the deck's own diagrams (slide 28's strip is lecture 2's learned templates, and slide 67's grid an MLP's). |

Not rendered from this deck: the title (1), administrative slides (2–3), the lecturer's timeline
(4), the course outline, recaps of lecture 2–4 figures (including slide 19's "This image by Nikita
is licensed under CC-BY 2.0" cat), the optimizer animation frame (8), section dividers, text,
formulas and the PyTorch documentation screenshots (95, 115; "PyTorch is licensed under BSD
3-clause."), build steps whose last step is rendered, and repeats of rendered figures. The slide
file's header lists every slide and the reason.

### Lecture 6 — Training CNNs and CNN Architectures

Deck: [lecture_6.pdf](https://cs231n.stanford.edu/slides/2025/lecture_6.pdf).
Rendered: 33 slides, in `raw/images/06-training-cnns-architectures/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 8 | Components grid; its pooling panel repeats lecture 5's downsampled activation image (224 to 112). Not credited. |
| 12 | Normalization-methods figure from Wu and He, "Group Normalization", ECCV 2018. No further credit. |
| 15, 16 | Dropout network drawings; slide 15 cites Srivastava et al., "Dropout: A simple way to prevent neural networks from overfitting", JMLR 2014. |
| 27 | ReLU and GELU chart: "Source: https://en.m.wikipedia.org/wiki/File:ReLU_and_GELU.svg"; cites Hendrycks et al., 2016. |
| 32 | Chart of ILSVRC winners compiled from the cited papers (Lin et al., Krizhevsky et al., Szegedy et al., He et al., Russakovsky et al., Shao et al., Hu et al.). |
| 35, 41 | VGG and AlexNet layer stacks and receptive-field grids, cited "[Simonyan and Zisserman, 2014]". |
| 47 | Training and test error curves of 20- and 56-layer plain networks, cited "[He et al., 2015]". Not otherwise credited. |
| 49, 52, 54, 55, 57 | Residual-block and ResNet diagrams, cited "[He et al., 2015]". |
| 65 | Cites He et al., "Delving Deep into Rectifiers", ICCV 2015. |
| 71, 72, 73, 74, 75 | Photograph of a tabby cat, not credited on these slides; slide 75's cutout examples cite DeVries and Taylor, "Improved Regularization of Convolutional Neural Networks with Cutout", arXiv 2017. |
| 78, 79 | AlexNet architecture figure (lecture 5 credits it "Figure copyright Krizhevsky, Sutskever, and Hinton, 2012. Reproduced with permission."), AlexNet's first-layer filters, and a grid of nearest-neighbour photographs. Not credited on these slides. |
| 82, 85 | Transfer-learning layer stacks; slides 80–82 cite Donahue et al., "DeCAF", ICML 2014, and Razavian et al., "CNN Features Off-the-Shelf", CVPR Workshops 2014. |
| 95 | "Illustration of Bergstra et al., 2012 by Shayne Longpre, copyright CS231n 2017"; cites Bergstra and Bengio, "Random Search for Hyper-Parameter Optimization", 2012. |
| 24, 26, 28, 61, 63, 90, 92, 93 | No third-party content identifiable: the deck's own plots, histograms and curves. |

Not rendered from this deck: the title, course logistics, the lecture overview, the lecture 5
recaps (slide 6 carries "Slide inspiration: Justin Johnson"), the weight-initialization divider,
text, equation and code slides, build steps whose last step is rendered, and repeats of rendered
figures. The slide file's header lists every slide and the reason.

### Lecture 7 — Recurrent Neural Networks

Deck: [lecture_7.pdf](https://cs231n.stanford.edu/slides/2025/lecture_7.pdf).
Rendered: 43 slides, in `raw/images/07-recurrent-neural-networks/`.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 7 | Loss curves from the course's own toy experiment ("Link to code (colab)", "Link to Ed Post"). No third-party content identified. |
| 12 | Screenshot of a Weights & Biases sweep page; "https://docs.wandb.ai/guides/track/app". |
| 68 | Page of Shakespeare's sonnets; link "Blogpost from Andrej Karpathy back in 2015!". Not otherwise credited. |
| 74 | Screenshot of the torvalds/linux repository page on GitHub. Not credited. |
| 76 | Screenshot of a code-generation demo with a rocketship image; "https://openai.com/blog/openai-codex/". Not otherwise credited. |
| 77–83 | "Karpathy, Johnson, and Fei-Fei: Visualizing and Understanding Recurrent Networks, ICLR Workshop 2016"; "Figures copyright Karpathy, Johnson, and Fei-Fei, 2015; reproduced with permission" (slides 78–83; slide 77 is the deck's own diagram). |
| 85 | "Figure from Karpathy et a, "Deep Visual-Semantic Alignments for Generating Image Descriptions", CVPR 2015; figure copyright IEEE, 2015. Reproduced for educational purposes." (printed "et a"). |
| 96 | Test photograph credited on slide 87: "This image is CC0 public domain". |
| 97 | "Captions generated using neuraltalk2. All images are CC0 Public domain: cat suitcase, cat tree, dog, bear, surfers, tennis, giraffe, motorcycle". |
| 98 | "Captions generated using neuraltalk2. All images are CC0 Public domain: fur coat, handstand, spider web, baseball". |
| 99 | Agrawal et al., "VQA: Visual Question Answering", ICCV 2015; Zhu et al., "Visual 7W", CVPR 2016; "Figure from Zhu et al, copyright IEEE 2016. Reproduced for educational purposes." |
| 101 | Das et al., "Visual Dialog", CVPR 2017; "Figures from Das et al, copyright IEEE 2017. Reproduced with permission." |
| 102 | Wang et al., "Reinforced Cross-Modal Matching and Self-Supervised Imitation Learning for Vision-Language Navigation", CVPR 2018; "Figures from Wang et al, copyright IEEE 2017. Reproduced with permission." (the year as printed). |
| 108, 113, 116 | Cite Bengio et al., IEEE Transactions on Neural Networks 1994, and Pascanu et al., ICML 2013. The diagrams and the tanh-derivative plot are not otherwise credited. |
| 124, 125, 126 | LSTM diagrams, cited "[Hochreiter et al., 1997]". |
| 130 | LSTM chain, a ResNet diagram (the same figure as lecture 6, slide 57, cited there to He et al., 2015) and the Highway Networks equations, citing Srivastava et al., "Highway Networks", ICML DL Workshop 2015. |
| 131 | Chart captioned "RWKV Scaling (arXiv)", and the title lines of the "Simplified State Space Layers for Sequence Modeling" and "Mamba: Linear-Time Sequence Modeling with Selective State Spaces" papers. No further credit. |
| 18, 22, 26, 28, 42, 45, 47, 50, 51, 54, 57, 58, 61, 65, 66, 104 | No third-party content identifiable: the deck's own diagrams (slide 28's tanh plot; slides 61–66's character-level model, slides the lecturer says the course has had "for quite a few years"). |

Not rendered from this deck: the title, course logistics, overview and text slides, the recap of
lecture 6's dropout figure (slide 4 cites Srivastava et al., JMLR 2014), text, equation and code
slides (including the min-char-rnn listing, slide 67, "Written by Andrej Karpathy (@karpathy) BSD
License", https://gist.github.com/karpathy/d4dee566867f8291f086), generated text, build steps
whose last step is rendered, and one repeat of a rendered figure. The slide file's header lists
every slide and the reason.

### Lecture 8 — Attention and Transformers

Deck: [lecture_8.pdf](https://cs231n.stanford.edu/slides/2025/lecture_8.pdf).
Rendered: 23 slides, in `raw/images/08-attention-transformers/`. The deck prints no copyright,
licence or permission line anywhere; its credits are paper citations.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 11 | Sequence-to-sequence diagram, citing Sutskever et al., "Sequence to sequence learning with neural networks", NeurIPS 2014. Not otherwise credited. |
| 19, 22, 23 | Attention diagrams, citing Bahdanau et al., "Neural machine translation by jointly learning to align and translate", ICLR 2015. Not otherwise credited. |
| 24, 27 | Attention-weight heatmap for English–French translation, citing Bahdanau et al., ICLR 2015, the paper the lecturer says the example is from (≈25:25). No copyright or licence line. |
| 91, 95 | Transformer block diagrams, citing Vaswani et al., "Attention is all you need," NeurIPS 2017; slide 95's sizes also cite Radford et al., 2019 (GPT-2) and Brown et al., 2020 (GPT-3). |
| 109 | A photograph of a cat cut into patches, and the ViT pipeline, citing Dosovitskiy et al., "An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale", ICLR 2021. The photograph is not credited. |
| 111, 112 | Post-norm and pre-norm block diagrams, citing Baevski & Auli, "Adaptive Input Representations for Neural Language Modeling", arXiv 2018. |
| 5, 29, 35, 46, 47, 57, 59, 61, 66, 82, 99, 120 | No third-party content identifiable: the deck's own diagrams (slide 5's two figures recur on slide 121; slides 29 and 35 recolour and annotate the attention diagram of slides 13–23; slide 120 carries no citation, while slides 113–118, which show the same block, cite Zhang and Sennrich, NeurIPS 2019, Shazeer, 2020, and Shazeer et al., 2017). |

Not rendered from this deck: the title, the administrative slide, the recap of lecture 7's
sequence-task figure, title-only and text slides, the matrix-shape and memory slides (68–78; slide
78 cites Dao et al., "FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness",
2022), build steps whose last step is rendered, and rendered figures repeated with new text or
equations (including slide 83's "Attention is All You Need" title box over slide 82). The slide
file's header lists every slide and the reason.

### Lecture 9 — Detection, Segmentation, Visualization, and Understanding

Deck: [lecture_9.pdf](https://cs231n.stanford.edu/slides/2025/lecture_9.pdf).
Rendered: 53 slides, in `raw/images/09-detection-segmentation-visualization/`. The deck prints no
licence for itself. Its credit lines for individual images are copied below; several slides carry
"Figure copyright …; reproduced with permission", a permission granted to the course that does not
pass to this repository.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 12 | A photograph of a cat cut into patches, and the ViT pipeline, citing Dosovitskiy et al., "An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale", ICLR 2021; "Cat image is free for commercial use under a Pixabay license". |
| 34, 39, 40, 42, 43, 64 | Photographs of a kitten and of two cows, with no credit line on these slides (slide 65 marks the same cow photograph "This image is CC0 public domain"). Slides 38–39 cite Farabet et al., TPAMI 2013, and Pinheiro and Collobert, ICML 2014; slide 43 cites Long, Shelhamer and Darrell, CVPR 2015, and Noh et al., ICCV 2015. |
| 60, 63 | The U-Net architecture figure, credited "Ronneberger et al. (2015) U-net Architecture". |
| 65, 70 | Photographs of a kitten and of cows, "This image is CC0 public domain". |
| 72, 74, 77 | Photographs of a kitten, of two dogs and a cat in front of a Christmas tree, and of a goose with goslings, with no credit line on these slides (slide 31 marks the four-task figure's images "This image is CC0 public domain"). |
| 78 | A photograph of a kitten and a puppy among flowers, with region proposals; citations to Alexe et al., TPAMI 2012, Uijlings et al., IJCV 2013, Cheng et al., CVPR 2014, and Zitnick and Dollár, ECCV 2014. The photograph is not credited. |
| 86 | The R-CNN figure: Girshick et al., "Rich feature hierarchies for accurate object detection and semantic segmentation", CVPR 2014. "Figure copyright Ross Girshick, 2015; source. Reproduced with permission." |
| 92 | The Fast R-CNN figure: Girshick, "Fast R-CNN", ICCV 2015. "Figure copyright Ross Girshick, 2015; source. Reproduced with permission." |
| 95, 96, 98 | A photograph of a kitten with anchor boxes, not credited on these slides. |
| 99 | The dogs-and-cat photograph with a grid of base boxes, citing Redmon et al., CVPR 2016 (YOLO), Liu et al., ECCV 2016 (SSD), and Lin et al., ICCV 2017 (focal loss). |
| 100, 104, 106 | The YOLO pipeline figure and a photograph of a dog, a bicycle and a car, credited "Redmon et al. 'You only look once: unified, real-time object detection (2015).'" |
| 107, 112 | The DETR pipeline figure and a photograph of two seagulls, citing Carion et al., "End-to-End Object Detection with Transformers", ECCV 2020. |
| 115 | The Faster R-CNN diagram with a mask branch, citing He et al., "Mask R-CNN", ICCV 2017; the same diagram is credited "Figure copyright 2015, Ross Girshick; reproduced with permission" on slides 167, 168 and 170. |
| 117 | The Mask R-CNN head on the Christmas-tree photograph, citing He et al., "Mask R-CNN", arXiv 2017. |
| 120, 121 | A photograph of a bedroom with a child, and mask targets; no credit line printed. |
| 122, 123 | Instance-segmentation and pose results on photographs, citing He et al., "Mask R-CNN", ICCV 2017. |
| 129 | First-layer filter visualizations of AlexNet, ResNet-18, ResNet-101 and DenseNet-121, citing Krizhevsky, arXiv 2014; He et al., CVPR 2016; Huang et al., CVPR 2017. |
| 131, 132 | Saliency maps and photographs from Simonyan, Vedaldi and Zisserman, "Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps", ICLR Workshop 2014. "Figures copyright Karen Simonyan, Andrea Vedaldi, and Andrew Zisserman, 2014; reproduced with permission." |
| 139, 140 | The CAM diagram and class activation maps, citing Zhou et al., "Learning Deep Features for Discriminative Localization", CVPR 2016. |
| 146 | Grad-CAM, guided backpropagation and occlusion maps of a dog and a cat, citing Selvaraju et al., "Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization", CVPR 2017. |
| 147 | ViT feature visualizations, citing Chen et al., ICLR 2022, and Paul and Chen, AAAI 2022, "Reproduced for educational purposes." |
| 158 | The kitten photograph with RoI Pool, citing Girshick, "Fast R-CNN", ICCV 2015. |
| 163, 164 | RoI Align diagrams over the kitten photograph, citing He et al., "Mask R-CNN", ICCV 2017. |
| 165 | Training- and test-time bar charts citing Girshick et al., CVPR 2014; He et al., ECCV 2014; Girshick, ICCV 2015. |
| 171 | The Faster R-CNN figure (Ren et al., NIPS 2015; credited "Figure copyright 2015, Ross Girshick; reproduced with permission" on slides 167, 168 and 170, not on 171). |
| 176, 177, 178 | A photograph of an elephant, a ReLU example, and maximally activating patches with guided-backprop images, citing Zeiler and Fergus, ECCV 2014, and Springenberg et al., ICLR Workshop 2015. "Figure copyright Jost Tobias Springenberg, Alexey Dosovitskiy, Thomas Brox, Martin Riedmiller, 2015; reproduced with permission." |
| 3, 46, 52, 56, 58, 169 | No third-party content identifiable: the deck's own diagrams and chart (slide 3's encoder and decoder; the unpooling and transposed-convolution grids; slide 169's test-time chart, which prints no citation). |

Not rendered from this deck: the title, the administrative, agenda, divider and text slides,
equations and matrices the slide file reproduces exactly, figures already rendered for an earlier
lecture (lecture 8's ViT and transformer tweaks, lecture 1's four-task figure, lecture 2's cat and
linear-classifier slides), build steps whose last step is rendered, and rendered figures repeated
with new text. The slide file's header lists every slide and the reason.

### Lecture 10 — Video Understanding

Deck: [lecture_10.pdf](https://cs231n.stanford.edu/slides/2025/lecture_10.pdf), a guest lecture by
Ruohan Gao. Rendered: 47 slides, in `raw/images/10-video-understanding/`. The deck prints no
licence for itself. Its credit lines are few ("This image is CC0 public domain", "Running video is
in the public domain", "Figure credit: …", "Slide credit: …", "Image Credit: Korbar et al.", "Video
source: BBC"); most third-party figures carry a paper citation only, copied below. Several slides
are stills of videos, which the PDF holds as one frame each.

| Slide | Third-party content (as identifiable from the slide) |
| --- | --- |
| 5, 7 | Frames of a video of a dog and a baby in a living room (slide 5 with detection and segmentation overlays). Slide 7: "This image is CC0 public domain"; slide 5 prints no credit line. |
| 9, 14, 15, 16, 18, 20, 21, 58, 70, 71, 75, 85 | Frames of a video of a person running, "Running video is in the public domain" (slides 8–9). Slide 9 also has a kitten photograph (marked "This image is CC0 public domain" on slide 4). Slides 16, 20 and 21 cite Karpathy et al., "Large-scale Video Classification with Convolutional Neural Networks", CVPR 2014, and slide 21 Ji et al., TPAMI 2010; 58 cites Ballas et al., ICLR 2016; 70–71 cite Wang et al., "Non-local neural networks", CVPR 2018; 75 cites Carreira and Zisserman, CVPR 2017; 85 cites Chao et al., CVPR 2018. |
| 37 | A mosaic of learned first-layer 3D filters; the slide gives no source. |
| 38, 42 | Sports-1M video frames with predicted labels, and a bar chart, citing Karpathy et al., CVPR 2014 (and, on 42, Tran et al., "Learning Spatiotemporal Features with 3D Convolutional Networks", ICCV 2015). |
| 46, 47, 48 | Photographs of a gymnast with optical flow, the two-stream architecture figure and a bar chart, citing Simonyan and Zisserman, "Two-stream convolutional networks for action recognition in videos", NeurIPS 2014. |
| 55, 63 | The deck's CNN-plus-RNN diagrams, citing Baccouche et al., 2011, and Donahue et al., CVPR 2015 (and, on 63, Ballas et al., ICLR 2016). |
| 61 | The recurrent convolutional network diagram, citing Ballas et al., "Delving Deeper into Convolutional Networks for Learning Video Representations", ICLR 2016. |
| 74, 76 | The inflated Inception block and a bar chart, citing Carreira and Zisserman, "Quo Vadis, Action Recognition? A New Model and the Kinetics Dataset", CVPR 2017. |
| 77 | Video frames of penguins and three architecture figures, citing Bertasius et al., ICML 2021; Arnab et al., ICCV 2021; Neimark et al., ICCV 2021; Fan et al., ICCV 2021; Li et al., CVPR 2022; Wang et al., CVPR 2023; Tong et al., NeurIPS 2022; Feichtenhofer et al., NeurIPS 2022. |
| 79, 81, 83 | The two-stream figure ("Figure credit: Simonyan and Zisserman", NeurIPS 2014) and optimized appearance and motion images, citing Feichtenhofer et al., CVPR 2018 and IJCV 2019, with "Slide credit: Christoph Feichtenhofers" (as printed, slide 80); frames of weightlifting and eye-makeup videos with no credit line. |
| 86 | Film frames from the AVA dataset, citing Gu et al., "AVA: A Video Dataset of Spatio-temporally Localized Atomic Visual Actions", CVPR 2018. |
| 92 | A video frame of two speakers and a separation diagram, citing thirteen papers from Gao et al., ECCV 2018, to Chen et al., CVPR 2023 (listed on the slide). |
| 96 | A video frame of two musicians, citing Gao and Grauman, "Co-Separating Sounds of Visual Objects", ICCV 2019. |
| 97 | Architecture figures from Nagrani et al., NeurIPS 2021; Zhang et al., CVPR 2022; Georgescu et al., ICCV 2023. |
| 98 | A film strip of a swimmer with clip classifiers, "Image Credit: Korbar et al." |
| 99 | Figures from Kondratyuk et al. (MoViNets), CVPR 2021; Korbar et al. (SCSampler), ICCV 2019; Feichtenhofer (X3D), CVPR 2020; and AdaMML, ICCV 2021 ("Pandal et al." as printed). |
| 100 | Video frames of cooking and an audio-preview diagram, citing Gao et al., "Listen to Look: Action Recognition by Previewing Audio", CVPR 2020. |
| 101 | Smart glasses, fisheye meeting frames and conversational graphs, citing Jia et al., CVPR 2024. |
| 102 | Figures from Lin et al. (Video-LLaVA), EMNLP 2024; Maaz et al. (Video-ChatGPT), ACL 2024; Zhang et al. (VideoLLaMA 3), arXiv 2025. |
| 22, 23, 28, 34, 36, 50, 53, 64, 78 | No third-party content identifiable: the deck's own diagrams and tables, and slide 78's chart, which prints no citation. |

Not rendered from this deck: the title, the guest lecturer's photograph, text slides, tables the
slide file reproduces exactly, figures already rendered for an earlier lecture (lecture 2's cat,
lecture 1's four-task figure, lecture 7's multi-layer RNN), video stills whose content is the video
or its sound (among them the BBC stills cited to McGurk and McDonald, 1976, and the VisualVoice
stills), build steps whose last step is rendered, and rendered figures repeated with new text. The
slide file's header lists every slide and the reason.
