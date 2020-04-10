---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Examining the Mapping Functions of Denoising Autoencoders in Singing Voice Separation"
authors: [Stylianos Mimilakis, Konstantinos Drossos, Estefanía Cano, Gerald Schuller]
date: 2019-08-20T21:56:02+08:00
doi: "10.1109/TASLP.2019.2952013"

# Schedule page publish date (NOT publication's date).
#publishDate: 2019-08-20T21:56:02+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "The goal of this article is to investigate what singing voice separation approaches based on neural networks learn from the data. We examine the mapping functions of neural networks based on the denoising autoencoder (DAE) model that are conditioned on the mixture magnitude spectra. To approximate the mapping functions, we propose an algorithm inspired by the knowledge distillation, denoted the neural couplings algorithm (NCA). The NCA yields a matrix that expresses the mapping of the mixture to the target source magnitude information. Using the NCA, we examine the mapping functions of three fundamental DAE-based models in music source separation; one with single-layer encoder and decoder, one with multi-layer encoder and single-layer decoder, and one using skip-filtering connections (SF) with a single-layer encoding and decoding. We first train these models with realistic data to estimate the singing voice magnitude spectra from the corresponding mixture. We then use the optimized models and test spectral data as input to the NCA. Our experimental findings show that approaches based on the DAE model learn scalar filtering operators, exhibiting a predominant diagonal structure in their corresponding mapping functions, limiting the exploitation of inter-frequency structure of music data. In contrast, skip-filtering connections are shown to assist the DAE model in learning filtering operators that exploit richer inter-frequency structures"
# Summary. An optional shortened abstract.
summary: ""

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: "https://ieeexplore.ieee.org/abstract/document/8892665"
url_code: "https://zenodo.org/record/2629650#.XmD700oRVEY"
url_dataset:
url_poster:
url_project:
url_slides:
url_source: https://arxiv.org/abs/1904.06157
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
