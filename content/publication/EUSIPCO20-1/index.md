---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Analyzing the potential of pre-trained embeddings for audio classification tasks"
authors: [ "Sascha Grollmisch", "Estefanía Cano", "Christian Kehling", "Michael Taenzer"]
date: 2020-01-03
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2019-08-01T19:28:09+08:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "In review"
publication_short: "In review"

abstract: "In the context of deep learning, the availability of large amounts of training data can play a critical role in a model's performance. Transfer learning has shown to be a powerful method in which models are first pre-trained for a task where abundant data is available, and then fine-tuned for a separate task where only a limited amount of data exists. In the past years, several models for audio classification have been pre-trained in a supervised or self-supervised fashion to learn complex feature representations, so called embeddings. These embeddings can then be extracted from smaller datasets and used to train subsequent classifiers. In the field of audio event detection (AED) for example, classifiers using these features have achieved high accuracy without the need of additional domain knowledge. 
This paper evaluates three state-of-the-art embeddings on six audio classification tasks from the fields of music information retrieval and industrial sound analysis, and presents a detailed overview of their potential. The embeddings are systematically evaluated by analyzing the influence of classifier architecture, fusion methods for file-wise predictions, amount of training data, and trained domain on classification accuracy. To better understand the effect of pre-training, results are also compared with those obtained with models trained from scratch. On average, OpenL3 embeddings performed best with a linear SVM classifier and for a reduced number of training examples they outperform the initial baseline."
# Summary. An optional shortened abstract.
summary: ""

tags: [Deep learning, Speech-music discrimination, Ensemble size classification, Instrument recognition]
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: 
url_code: https://github.com/ACMUS-MIR/ACMus-Models
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
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

Detailed results can be found in [here](https://acmus-mir.github.io/embeddings-20/). 

