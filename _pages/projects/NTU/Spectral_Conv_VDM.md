---
layout: single
permalink: /projects/NTU/Spectral_Conv_VDM.html
excerpt: Supervised by Dr. Mao-Pei Tsui (NTU) & Dr. Hau-Tieng Wu (Duke)
header:
  overlay_image: /images/projects/subheads.jpg
  overlay_filter: 0.5
title: "Spectral Convergence of Vector Diffusion Map"
author_profile: true
comments: true
---

## Introduction
Vector diffusion maps (VDM) is a tools for organizing complex data sets, embedding them in a low dimensional space, and interpolating and regressing vector fields over the data. VDM is a mathematical and algorithmic generalization of diffusion maps, which is a non-linear dimensionality reduction method based on eigenvectors and eigenvalues of discrete graph Laplacians. The following figure shows the relation between DM and VDM.
  <center>
    <img src="/images/projects/vdm/relation.png" width="500" alt="diag of sf"/>
    <figcaption>Figure: The relation between DM and VDM</figcaption>
  </center>

  In recently paper, pointwise convergence of the graph connection Laplacian to the connection Laplacian of the tangent bundle is proved in Singer and Wu (2011). Furthermore, the eigenvectors and eigenvalues of the graph Laplacian converge to the eigenfunctions and eigenvalues of the Laplace-Beltrami operator in $$L^2$$ sense is proved in Singer & Wu (2015). Thus, this project is focus on proving the spectral convergence of VDM in $$L^\infty$$ sense.

|     | pointwise conv                        | spectral conv in $$L^2$$ | spectral conv in $$L^\infty$$ |
|-----|-------------------------------------------|--------------------------|-------------------------------|
| DM  | Coifman & Lafon  (2006) and Singer (2006) | Belkin & Niyogi  (2006)  | Dunson, Wu & Wu (2019)        |
| VDM | Singer & Wu (2011)                        | Singer & Wu (2015)       | this project                  |


## Main Idea of Proof
Due to the results not being published yet, I cannot disclose too much information at this point. Hence, we sketched the proof here.
  <center>
    <img src="/images/projects/vdm/vector_conv.png" width="500" alt="diag of sf"/>
    <figcaption>Figure: The main steps of proof</figcaption>
  </center>


## References
1. M. Belkin and P. Niyogi, _Convergence of laplacian eigenmaps_, (2006).
2. R. R. Coifman and S. Lafon, _Diffusion maps_, (2006).
3. D. B. Dunson, H.-T. Wu, and N. Wu, _Spectral convergence of graph laplacian and heat kernel reconstruction
in l infinity norm from random samples_, (2019).
4. A. Singer, _From graph to manifold laplacian: The convergence rate_, (2006).
4. A. Singer and H.-T. Wu, _Spectral convergence of the connection laplacian from random samples_, (2015).
5. A. Singer and H.-T. Wu, _Vector diffusion maps and the connection laplacian_, (2011).