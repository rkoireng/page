---
layout: post
title: Enhanced Receiver Function
tags: [Katex, Mermaid, Markdown]
feature-img: "assets/img/feature-img/Cas.png"
thumbnail: "assets/img/feature-img/Cas.png"
categories: Demo
---

## Problem Statement:
Receiver function (RF) is a useful technique to image seismic discontinuties at the crust and mantle. Computation of RF involves deconvolving either the radial or transverse component with the vertical component seismogram. The depth, anisotropic properties and seismic parameter of the discontinuities can be derived from RFs computed for different backazimuth and slowness. Nonetheless, the ill-posed deconvolution process nuisances that are influence by the earthquake source signature, regularisation and seismic noise. These pseudo-random non-Gaussian nuisances distort the RFs and significantly affects the RF analysis. These nuisances has the same frequency band with the converted waves from seismic discontinuities making it difficult to filtered out.
## Methodology:

We used a deep-learning network, symmetric autoencoders (SymAE), to separate the nuisances from useful converted waves. Basically, SymAE learns to represent a group of RFs from similar backazimuth as two latent code: coherent code and nuisance code. The coherent code encodes the coherent converted waves and nuisnace code encodes the varying nuisances. SymAE allow us to generate virtual RFs that are devoid of nuisance by using same nuisance code in all RFs and subtracting the mean from each RF.

{% include aligner.html images="feature-img/symae.jpg" column=1 %}

## Synthetic Results:

{% include aligner.html images="feature-img/synthetic.jpg" column=1 %}

## Real Data Results:

{% include aligner.html images="feature-img/Casfig.png" column=1 %}

{% include aligner.html images="feature-img/CasRF.jpg" column=1 %}

## For more detail read: [https://arxiv.org/abs/2411.14182v1](https://arxiv.org/abs/2411.14182v1)
