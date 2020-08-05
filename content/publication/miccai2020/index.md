+++
title = "Semi-supervised Medical Image Classification with Global Latent Mixing"

# Date first published.
date = "2020-05-22"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Prashnna K. Gyawali", "Sandesh Ghimire", "<b>Pradeep Bajracharya</b>", "Zhiyuan Li", "Linwei Wang"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "In *Medical Image Computing and Computer Assisted Intervention*. "

# Abstract and optional shortened version.
abstract = "Computer-aided diagnosis via deep learning relies on large-scale annotated data sets, which can be costly when involving expert knowledge. Semi-supervised learning (SSL) mitigates this challenge by leveraging unlabeled data. One effective SSL approach is to regularize the local smoothness of neural functions via perturbations around single data points. In this work, we argue that regularizing the global smoothness of neural functions by filling the void in between data points can further improve SSL. We present a novel SSL approach that trains the neural network on linear mixing of labeled and unlabeled data, at both the input and latent space in order to regularize different portions of the network. We evaluated the presented model on two distinct medical image data sets for semi-supervised classification of thoracic disease and skin lesion, demonstrating its improved performance over SSL with local perturbations and SSL with global mixing but at the input space only."

abstract_short = "Computer-aided diagnosis via deep learning relies on large-scale annotated data sets, which can be costly when involving expert knowledge."

# Featured image thumbnail (optional)
image_preview = "miccai2020.png"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Links (optional).
url_pdf = "https://arxiv.org/abs/2005.11217"
url_preprint = ""
url_code = "https://github.com/Prasanna1991/LatentMixing"
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "miccai2020.png"
caption = "Schematic Diagram of the presented SSL method"

+++