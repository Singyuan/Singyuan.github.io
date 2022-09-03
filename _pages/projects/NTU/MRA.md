---
layout: single
permalink: /projects/NTU/MRA.html
excerpt: Supervised by Dr. Mao-Pei Tsui (NTU) & Dr. Hau-Tieng Wu (Duke)
header:
  overlay_image: /images/projects/subheads.jpg
  overlay_filter: 0.5
title: "Predict Sleep Stages via Multi-Resolution Analysis"
author_profile: true
comments: true
---

## Introduction
According to American Academy of Sleep Medicine (AASM), the sleep dynamics can be divided into two broad stages, the rapid eye movement (REM) and the non-rapid eye movement (NREM), and the NREM stage is further divided into shallow sleep (stage N1 and N2) and deep sleep (stage N3). 
<center>
    <img src="/images/projects/DM/sleeepstages.png" width="300" alt="structure"/>
</center>

Now, we hope to use physiological signals to predict sleep stages. The physiological signals is as following.
<center>
    <img src="/images/projects/DM/multich.png" width="500" alt="structure"/>
</center>
In fact, it is difficult to classify different sleep stages by one signals. Hence, it is important to develop sensor fusion method.
<center>
    <img src="/images/projects/DM/hard.png" width="500" alt="structure"/>
</center>

## Task
Actually, there have been many proposed algorithms which is aim at fusion <b>two</b> signals, for instance CCA. Hence, we proposed another concept to fusion 3+ signals.
<center>
    <img src="/images/projects/DM/fuse3up.png" width="500" alt="structure"/>
</center>

## Methodology
<center>
    <img src="/images/projects/DM/method.png" width="500" alt="structure"/>
</center>
According to above image, there are two key step in this step, feature extraction and dimension reduction.<br>

**Feature Extraction**
We use scattering transformation which is based on wavelet transformation. Since the uncertainty principle, the resolution of wavelet transformation should be logarithmically spaced grid. Please refer to my [note](https://hackmd.io/@singyuan/rJhQ3zDat) for more detail. Take a 90 seconds signals for instance,
<center>
    <img src="/images/projects/DM/cwt.png" width="500" alt="structure"/>
</center>

Moreover, the scalogram plot as following
<center>
    <img src="/images/projects/DM/dwt.png" width="500" alt="structure"/>
</center>

Therefore, the main idea is to deal with the high frequency zone.
<center>
    <img src="/images/projects/DM/scattering.png" width="500" alt="structure"/>
</center>
Please refer to Andén & Mallat [(2013)](https://arxiv.org/abs/1304.6763) for more detail.

**Dimension Reduction**
We use multi-resolution analysis to reduce dimension, which is based on SA method. The main idea of SA method is to recover the common and difference of two manifold which the data is lie on.
<center>
    <img src="/images/projects/DM/sa.png" width="500" alt="structure"/>
</center>
Please refer to Shnitzer <i>et al.</i> [(2018)](https://arxiv.org/abs/1808.07312) for more detail. However, the multi-resolution analysis will be added when the paper is published.

## Result
So far the result is in my [slides](./../../../pdf/projects/DM/MRA4pub.pdf). We will update when the paper is published.



## References
  1. G.-R. Liu, Y.-L. Lo, J Malik, Y.-C. Sheu, H.-T. Wu, <i>Diffuse to fuse EEG spectra -- intrinsic geometry of sleep dynamics for classification.</i>, (2018).
  2. T. Shnitzer, M. Ben-Chen, L. Guibas, R. Talmon, H.-T. Wu, <i>Recovering Hidden Components in Multimodal Data with Composite Diffusion Operators.</i>, (2018).
  3. J. Andén & S. Mallat, <i>Deep Scattering Spectrum.</i>, (2013).

## Material

  [Slides](./../../../pdf/projects/DM/MRA4pub.pdf)