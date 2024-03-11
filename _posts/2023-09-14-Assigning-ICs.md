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

Read the rest of this post on my old blog at
<https://mandymejia.wordpress.com/2023/09/14/assigning-independent-components-to-canonical-brain-networks/>.
