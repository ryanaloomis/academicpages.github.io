---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
redirect_from:
  - /software
---
Here are some tools I've developed to better analyze and image radio interferometric data:

_VISIBLE_ - spectral line detection through matched filtering
======
_VISIBLE_ is a Python code which uses matched filtering to strongly boost the SNR of weak spectral lines.

Modern radio interferometers enable observations of spectral lines with unprecedented spatial resolution and sensitivity. In spite of these technical advances, many lines of interest are intrinsically weak and therefore necessitate detection and analysis techniques specialized for the low SNR regime. Matched filters can leverage knowledge of the source structure and kinematics to increase sensitivity of spectral line observations. Application of the filter in the native Fourier domain improves SNR while simultaneously avoiding the computational cost and ambiguities associated with imaging, making matched filtering a fast and robust method for weak spectral line detection.

Check out [the paper]() where we demonstrate the method and describe different options for generating filter kernels. _VISIBLE_ is publicly available on both [Github]() and the [Anaconda Cloud]().

_vis_sample_ - fast visibility sampling in Python
======
Analysis of interferometric data often requires transforming between the image plane and the incompletely sampled _uv_ plane (ie when comparing a model to data). The _uvmodel_ task accomplishes this purpose in Miriad, but is not easily incorporated into a Python script.

To fill this niche, we have developed _vis_sample_, a Python-based implementation of the visibility sampling algorithm behind _uvmodel_. By using Peter Williams' [casa-python package](), it natively interfaces with CASA Measurement Sets, as well as UVFITS files. Fast and simple to use, _vis_sample_ is especially useful for MCMC analysis of interferometric datasets.

_vis_sample_ is publicly available on both [Github]() and the [Anaconda Cloud](), and is a dependency for _VISIBLE_.

\*IN DEVELOPMENT\* _Adaptive Briggs weighting_ - a new weighting scheme optimized for imaging extended sources
======
In his [PhD thesis](), Dan Briggs showed that an imaging weighting scheme which tunes between the two extremes of natural (highest SNR) and uniform (highest resolution) weighting can recover most of the benefits of each (aka 'robust' weighting). This method is now essentially the default weighting for most interferometric imaging. The derivation of robust weighting assumes, however, that the observations are of a point source, an assumption which is insufficient for many sources as modern interferometers provide increasing resolution. 

We have derived a more general form of traditional Briggs robust weighting, which is adaptive to the source being observed and properly incorporates the source visibility contributions into the weight of any given grid cell, maximizing SNR. As with robust weighting, the weights are tunable between this matched filter 'natural' weighting and uniform weighting. In the limit of a point source, robust weighting is recovered, while the weighting scheme outperforms robust weighting for all other source structures and offers significant benefits over the conventional Gaussian tapering of weak sources.

Source code and a CASA implementation coming soon to Github!