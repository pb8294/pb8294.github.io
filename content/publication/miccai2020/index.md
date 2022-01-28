---
title: Semi-supervised Medical Image Classification with Global Latent Mixing
date: '2020-05-22'
authors:
  - Prashnna K. Gyawali
  - Sandesh Ghimire
  - admin
  - Zhiyuan Li
  - Linwei Wang
publication_types: ['1']
publication: 'In *Medical Image Computing and Computer Assisted Intervention*. '
abstract: 
  Computer-aided diagnosis via deep learning relies on large-scale annotated
  data sets, which can be costly when involving expert knowledge.
  Semi-supervised learning (SSL) mitigates this challenge by leveraging
  unlabeled data. One effective SSL approach is to regularize the local
  smoothness of neural functions via perturbations around single data points. In this work, we argue that regularizing the global smoothness of neural functions by filling the void in between data points can further improve SSL. We present a novel SSL approach that trains the neural network on linear mixing of labeled and unlabeled data, at both the input and latent space in order to regularize different portions of the network. We evaluated the presented model on two distinct medical image data sets for semi-supervised classification of thoracic disease and skin lesion, demonstrating its improved performance over SSL with local perturbations and SSL with global mixing but at the input space only.

summary: 
  In this work, we argue that regularizing the global smoothness of neural functions by filling the void in between data points can further improve SSL. We present a novel SSL approach that trains the neural network on linear mixing of labeled and unlabeled data, at both the input and latent space in order to regularize different portions of the network.

image_preview: miccai2020.png
selected: true
projects: []
url_pdf: 'https://arxiv.org/abs/2005.11217'
url_preprint: ''
url_code: 'https://github.com/Prasanna1991/LatentMixing'
url_dataset: ''
url_project: ''
url_slides: ''
url_video: ''
url_poster: ''
url_source: ''
math: true
highlight: true
header:
  image: miccai2020.png
  caption: Schematic Diagram of the presented SSL method

---
<!-- 
{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Supplementary notes can be added here, including [code, math, and images](https://wowchemy.com/docs/writing-markdown-latex/). -->
