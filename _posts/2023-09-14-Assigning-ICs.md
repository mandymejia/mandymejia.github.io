---
title: "Assigning independent components to canonical brain networks"
author: "Mandy Mejia"
date: "2023-09-14"
output:
  md_document:
    variant: markdown_github
    preserve_yaml: true
---

A lot of the work my group does these days focuses on independent
component analysis (ICA). ICA is a blind-source separation algorithm
that is a popular way to analyze fMRI data. With ICA, you get a set of
spatial independent component (IC) maps and a “mixing matrix” that
contains the temporal activity associated with each IC. From that mixing
matrix, you can compute functional connectivity (FC) matrices, either
static or dynamic. When it comes to displaying FC matrices, we typically
want to group the ICs by brain network, which results in a nice
block-diagonal structure that aids in visual interpretation. We may also
want to summarize FC or the spatial ICs by network.

Therefore, we often need to “assign” ICs to a canonical network or area
of the brain. While there are many ways to approach this, my group has
been experimenting with this for a while, and we finally have a
procedure that works pretty well. In this post, I will describe our
approach and show some examples.

If you happen to be working with the Human Connectome Project group ICA
at the 25- or 100-component resolution, this recent
[preprint](https://arxiv.org/abs/2311.03791) describes the IC assignment
method and reports the final IC network labels. Please cite that paper
if you use those assignments or adopt our methodology. All of the
figures shown below are generated using our our ciftiTools R package,
which is freely available on Github and CRAN. Links available at
[statmindlab.com/software](https://www.statmindlab.com/software). If you
use ciftiTools, please cite Damon Pham’s
[paper](https://www.sciencedirect.com/science/article/pii/S1053811922000076)
describing and illustrating the software.

Here we are attempting to match our ICs to the well-known 17 Yeo
cortical networks and the Freesurfer subcortical parcels. However, the
procedure described below should work well for other sets of
networks/regions.

<span style="color:red"> ***… this post was originally written on my old
blog. Read the full post
[here](https://mandymejia.wordpress.com/2023/09/14/assigning-independent-components-to-canonical-brain-networks/).
*** </span>
