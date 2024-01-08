---
layout: single
permalink: /projects/NTU/bayesian_PD.html
excerpt: Supervised by Dr. Chun-Hao Yang (NTU)
header:
  overlay_image: /images/projects/subheads.jpg
  overlay_filter: 0.5
title: Bayesian Shrinkage Estimation for Persistent Diagram
author_profile: true
comments: true
---

## Introduction
Persistent homology is a powerful tool in computational topology for studying the evolution of topological features in data sets across different scales. It provides a way to analyze the lifespan or persistence of features such as connected components, voids, and holes.

The key idea is to examine the changes in homological features as a parameter (often related to scale) varies. Persistent homology is particularly useful for capturing topological information that persists through multiple scales, offering a robust representation of the underlying structures in the data.

The _persistent diagram_ is a visual representation of the persistent homology results. It consists of points in the plane, where each point corresponds to a homological feature. The x-coordinate represents the scale at which the feature is born, and the y-coordinate represents the scale at which it dies.

For instance, the following figure shows the persistence diagram of the point cloud drawn from a 2-dim sphere; the black
filled circles correspond to $$k = 0$$, the red triangles correspond to $$k = 1$$, and the blue squares
correpond to $$k = 2$$.

  <center>
    <img src="/images/projects/bayes_PD/PD_sphere.png" width="500" alt="diag of unet"/>
    <figcaption>Figure: persistence diagram of the point cloud on sphere.</figcaption>
  </center>


## References
1. F. Chazal & B. Michel, _An introduction to Topological Data Analysis: fundamental and practical aspects for data scientists_, (2021).
2. L. Wasserman, _Topological Data Analysis_, (2018).


