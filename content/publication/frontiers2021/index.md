---
title: 
  Fast Posterior Estimation of Cardiac Electrophysiological Model Parameters via
  Bayesian Active Learning
date: '2021-10-25'
authors:
  - Md Shakil Zaman
  - Jwala Dhamala
  - admin
  - John L. Sapp
  - B Milan Horácek
  - Katherine C Wu
  - Natalia A Trayanova
  - Linwei Wang
publication_types:
  - '2'
publication: 'In *frontiers in Physiology*. '
abstract: 
  Probabilistic estimation of cardiac electrophysiological model parameters serves an important step toward model personalization and uncertain quantification. The expensive computation associated with these model simulations, however, makes direct Markov Chain Monte Carlo (MCMC) sampling of the posterior probability density function (pdf) of model parameters computationally intensive. Approximated posterior pdfs resulting from replacing the simulation model with a computationally efficient surrogate, on the other hand, have seen limited accuracy. In this study, we present a Bayesian active learning method to directly approximate the posterior pdf function of cardiac model parameters, in which we intelligently select training points to query the simulation model in order to learn the posterior pdf using a small number of samples. We integrate a generative model into Bayesian active learning to allow approximating posterior pdf of high-dimensional model parameters at the resolution of the cardiac mesh. We further introduce new acquisition functions to focus the selection of training points on better approximating the shape rather than the modes of the posterior pdf of interest. We evaluated the presented method in estimating tissue excitability in a 3D cardiac electrophysiological model in a range of synthetic and real-data experiments. We demonstrated its improved accuracy in approximating the posterior pdf compared to Bayesian active learning using regular acquisition functions, and substantially reduced computational cost in comparison to existing standard or accelerated MCMC sampling.
summary: 
  We present a Bayesian active learning method to directly approximate the posterior pdf function of cardiac model parameters, in which we intelligently select training points to query the simulation model in order to learn the posterior pdf using a small number of samples. We integrate a generative model into Bayesian active learning to allow approximating posterior pdf of high-dimensional model parameters at the resolution of the cardiac mesh.
image_preview: frontiers.jpeg
selected: true
projects: []
url_pdf: 'https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8573318/'
url_preprint: ''
url_code: ''
url_dataset: ''
url_project: ''
url_slides: ''
url_video: ''
url_poster: ''
url_source: ''
math: true
highlight: true

---