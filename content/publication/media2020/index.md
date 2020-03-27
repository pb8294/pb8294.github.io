+++
title = "Embedding High-dimensional Bayesian Optimization via Generative Modeling: Parameter Personalization of Cardiac Electrophysiological Models"

# Date first published.
date = "2020-02-27"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Jwala Dhamala", "Pradeep Bajracharya", "Hermenegild J Arevalo", "B Milan Horácek", "Katherine C Wu", "Natalia A Trayanova", "Linwei Wang"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "In *Medical Image Analysis*. "

# Abstract and optional shortened version.
abstract = "The estimation of patient-specific tissue properties in the form of model parameters is important for personalized physiological models. Because tissue properties are spatially varying across the underlying geometrical model, it presents a significant challenge of high-dimensional (HD) optimization at the presence of limited measurement data. A common solution to reduce the dimension of the parameter space is to explicitly partition the geometrical mesh. In this paper, we present a novel concept that uses a generative variational auto-encoder (VAE) to embed HD Bayesian optimization into a low-dimensional (LD) latent space that represents the generative code of HD parameters. We further utilize VAE-encoded knowledge about the generative code to guide the exploration of the search space. The presented method is applied to estimating tissue excitability in a cardiac electrophysiological model in a range of synthetic and real-data experiments, through which we demonstrate its improved accuracy and substantially reduced computational cost in comparison to existing methods that rely on geometry-based reduction of the HD parameter space."

abstract_short = "The estimation of patient-specific tissue properties in the form of model parameters is important for personalized physiological models."

# Featured image thumbnail (optional)
image_preview = "media2020.jpg"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Links (optional).
url_pdf = "https://www.sciencedirect.com/science/article/abs/pii/S1361841520300360"
url_preprint = ""
url_code = ""
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
image = "media2020.jpg"
caption = "Graphical Abstract"

+++