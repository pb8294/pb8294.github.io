+++
title = "Fast Posterior Estimation of Cardiac Electrophysiological Model Parameters via Bayesian Active Learning"

# Date first published.
date = "2020-05-22"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Md Shakil Zamen", "Jwala Dhamala", "<b>Pradeep Bajracharya</b>", "John L Sapp", "B Milan Horácek", "Katherine C Wu", "Natalia A Trayanova", "Linwei Wang"]

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
publication = "In *Medical Image Computing and Computer Assisted Intervention*. "

# Abstract and optional shortened version.
abstract = "Probabilistic estimation of cardiac electrophysiological model parameters serves an important step
towards model personalization and uncertain quantification. The expensive computation associated
with these model simulations, however, makes direct Markov Chain Monte Carlo (MCMC) sampling
of the posterior probability density function (pdf) of model parameters computationally intensive.
Approximated posterior pdfs resulting from replacing the simulation model with a computationally
efficient surrogate, on the other hand, have seen limited accuracy. In this paper, we present a Bayesian
active learning method to directly approximate the posterior pdf function of cardiac model parameters,
in which we intelligently select training points to query the simulation model in order to learn the
posterior pdf using a small number of samples. We integrate a generative model into Bayesian
active learning to allow approximating posterior pdf of high-dimensional model parameters at the
resolution of the cardiac mesh. We further introduce new acquisition functions to focus the selection
of training points on better approximating the shape rather than the modes of the posterior pdf
of interest. We evaluated the presented method in estimating tissue excitability in a 3D cardiac
electrophysiological model in a range of synthetic and real-data experiments. We demonstrated its
improved accuracy in approximating the posterior pdf compared to Bayesian active learning using
regular acquisition functions, and substantially reduced computational cost in comparison to existing
standard or accelerated MCMC sampling."

abstract_short = "Probabilistic estimation of cardiac electrophysiological model parameters serves an important step
towards model personalization and uncertain quantification."

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Links (optional).
url_pdf = ""
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
image = ""
caption = ""

+++