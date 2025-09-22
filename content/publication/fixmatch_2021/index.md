---
title: "Improving semi-supervised learning for audio classification with fixmatch"
authors:
- Sascha Grollmisch
- admin

author_notes: ""
date: "2021-07-28T00:00:00Z"

# Schedule page publish date (NOT publication's date).
#publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "*MDPI Electronics*"
publication_short: ""

abstract: Including unlabeled data in the training process of neural networks using Semi-Supervised Learning (SSL) has shown impressive results in the image domain, where state-of-the-art results were obtained with only a fraction of the labeled data. The commonality between recent SSL methods is that they strongly rely on the augmentation of unannotated data. This is vastly unexplored for audio data. In this work, SSL using the state-of-the-art FixMatch approach is evaluated on three audio classification tasks, including music, industrial sounds, and acoustic scenes. The performance of FixMatch is compared to Convolutional Neural Networks (CNN) trained from scratch, Transfer Learning, and SSL using the Mean Teacher approach. Additionally, a simple yet effective approach for selecting suitable augmentation methods for FixMatch is introduced. FixMatch with the proposed modifications always outperformed Mean Teacher and the CNNs trained from scratch. For the industrial sounds and music datasets, the CNN baseline performance using the full dataset was reached with less than 5% of the initial training data, demonstrating the potential of recent SSL methods for audio data. Transfer Learning outperformed FixMatch only for the most challenging dataset from acoustic scene classification, showing that there is still room for improvement.

# Summary. An optional shortened abstract.
# summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Research
featured: false

hugoblox:
  ids:
    doi: 10.3390/electronics10151807

links:
  - type: pdf
    url: https://www.mdpi.com/2079-9292/10/15/1807/pdf?version=1627550343
  #- type: code
  #  url: https://github.com/ACMUS-MIR/publications-resources/tree/master/TISMIR2021
  #- type: dataset
  #  url: https://zenodo.org/records/4791394
  #- type: poster
  #  url: ""
  #- type: project
  #  url: ""
  #- type: slides
  #  url: https://www.slideshare.net/
  #- type: source
  #  url: ""
  #- type: video
  #  url: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
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
reading_time: False
share: False
---



