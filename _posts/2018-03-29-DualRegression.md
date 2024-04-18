---
title: "The Role of Centering in Dual Regression"
author: "Mandy Mejia"
date: "2018-03-29"
knit: (function(inputFile, encoding) { 
      rmarkdown::render(inputFile,
                        encoding=encoding, 
                        output_file=file.path('~/Documents/Github/mandymejia.github.io/_posts/', '2018-03-29-DualRegression.md')) })
output:
  md_document:
    variant: gfm
    preserve_yaml: true
---

Dual regression is maybe the simplest way to obtain subject-specific
estimates of ICA-based resting-state networks (RSNs). RSNs are regions
of the brain that tend to act in a coordinated manner in the absence of
a specific task, such as the three shown below (from a 50-component ICA
of the Human Connectome Project).

Popular ICA toolboxes for fMRI analysis like GIFT and MELODIC can
perform dual regression, but such a simple approach is also
straightforward to implement one one’s own. I end up doing this a lot
(and would love to hear in the comments whether others do too or prefer
to use existing implementations). This post is about the important role
of centering in dual regression, which is easy to overlook (at least for
me) when implementing this simple technique.

<span style="color:red"> ***… this post was originally written on my old
blog. Read the full post
[here](https://mandymejia.wordpress.com/2018/03/29/the-role-of-centering-in-dual-regression/).
*** </span>
