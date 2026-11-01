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

The lectures and slide decks are the work of Fei-Fei Li, Ehsan Adeli, Zane Durante and the
CS231N course staff (Stanford University, Spring 2025). They are published through the course
website, <https://cs231n.stanford.edu/2025/>, with the lecture videos on YouTube.

As checked on 2026-11-01, no licence, copyright or reuse statement appears on the course
website's index, schedule or project pages, and none covering the decks as a whole is printed in
the Lecture 1 or Lecture 2 decks (lecture 2 checked on 2026-11-02). Publicly downloadable is not the same as licensed. Absent an express grant
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
