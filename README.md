# MVP - Microbiome Visualization Project

This is an opinionated essay about good and bad practices in the visualization of microbiome data. Here, I'll flag some issues I find with certain types of visualizations, while providing alternatives. I hope this exercise helps me (and hopefully others too) to become **MVPs** in generating effective microbiome visualizations.

This work is inspired by [Friends Don't Let Friends Make Bad Graphs](https://github.com/cxli233/FriendsDontLetFriends/tree/main?tab=readme-ov-file), so I'll keep the overlap at the lowest.

The folder `data/` contains the raw data used in the generation of the plots below. The code to generate the figures in `.Rmd` format can be found in the `scripts/` folder, and the output files are stored in `figures/`.


#### **About me**
* Author: Benjamin Valderrama, PhD student at APC microbiome Ireland.
* Links: [Personal Website](https://benjamin-valderrama.github.io/) | [Google scholar](https://scholar.google.com/citations?user=fteDslYAAAAJ&hl=es) | [BlueSky](https://bsky.app/profile/bvalderrama.bsky.social) 


# Table of contents

1. [Making sense of cluttered PCAs](https://github.com/Benjamin-Valderrama/MVP/#1-making-sense-of-cluttered-pcas)

# 1. Making sense of cluttered PCAs

<div align="justify"> Principal Component Analysis (PCA) plots are ubiquitous in the microbiome literature, thus it has to be the first visualization to cover. They are a simplified 2D representation of the multiple differences between samples. Thus, higher distances between any pair of samples represent higher dissimilarity between them in the (original) multidimensional space. 


Then task of this visualization is to accurately show distances between samples or groups. It's easy to see than when we deal with many samples (like in the example below), PCA plots are very cluttered making it impossible to determine those distances.</div>

![cluttered_pcas](https://github.com/Benjamin-Valderrama/MVP/blob/main/figures/alternatives_to_cluttered_pca.png)


<div align="justify"> One solution is to add boxplots (or density plots) on the sides of the principal components, to show the distribution of each group along them. This is a fairly common solution in the literature, and it is often enough. 

Although less popular, another solution is to make bins on the PCA space, plot all data in the background and then add on top the distribution of the samples from each group, as shown in the three plots below.</div>