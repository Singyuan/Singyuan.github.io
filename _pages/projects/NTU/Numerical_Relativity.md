---
layout: single
permalink: /projects/NTU/Numerical_Relativity.html
excerpt: Supervised by Dr. Mao-Pei Tsui (NTU)
header:
  overlay_image: /images/projects/subheads.jpg
  overlay_filter: 0.5
title: "A Numerical Study of Einstein Scalar Field Equations in Spherically Symmetric Spacetime"
author_profile: true
comments: true
---

## Introduction

  Choptuik presented a numerical study of spherically symmetric collapse of Einstein scalar field equations. Given a initial scalar field $$\psi(r)$$ and zero initial velocity of such scalar field $$\psi^\prime (r)=0$$ in space (radius coordinates) $$r$$, we focus the scalar fields evolve in the future, especially near origin.
  <center>
    <img src="/images/projects/nr/bang.jpg" width="300" alt="diag of sf"/>
    <figcaption>Figure: Schematic diagram of scalar fields</figcaption>
  </center>
  The following video is shown how the scalar fields transport. This is weak solution because the incoming scalar field can pass through origin, which cannot collapse the spacetime.
  <center>
  <video width="480" height="320" controls="controls">
    <source src="/images/projects/nr/sf.mp4" type="video/mp4">
  </video>
  </center>
  Hence, we want to know how large of the amplitude $$A$$ of the initial scalar fields $$\psi_A(r)$$ will collapse the spacetime, <i>i.e.</i> incoming scalar fields "freeze" at origin. In this thesis, the initial scalar field is considered as $$\psi_A(r)=Ar^2e^{-(r-5)^2}$$. The amplitude of above video is $$A=0.0001$$.

## Goals
  The spherically symmetric metric can be wriiten as $$g=\alpha(r,t)^2dt^2+a^2(r,t)dr^2+r^2d\Omega^2$$. Then, we use Einstein scalar fields $$G_{\mu\nu}=8\pi T_{\mu\nu}$$to solve functions $$a(r,t)$$ and $$\alpha(r,t)$$.<br>
  It seems that the numerical simulation of such evolution system is quite trivial. However, we have to face the following problem when we apply finite difference method.
  
  * <b>Stability and Converge Problem</b>: The evolution system is highly nonlinear system so the high order numerical method might not converge.

  <center>
    <img src="/images/projects/nr/dmdr4.png" width="250" alt="diag of sf"/>
    <figcaption>Figure: The algorithm is not converge.</figcaption>
  </center>

  * <b>Outer Boundary Problem</b>: The computational domain is a finite region but the real space is infinite region. How to impose artificial boundary represents infinite space, which cannot violate the constraint equations.

  <center class="half">
    <img src="/images/projects/nr/fail1.png" width="200" alt="ori img"/><img src="/images/projects/nr/fail2.png" width="200" alt="overfit label"/> 
    <figcaption>Figure: This is a system <b>without</b> outer boundary condition. The RHS subfigure is next moment of LHS subfigure. There are a large pulse coming from outside at right boundary.</figcaption>
  </center>

  * <b>Inner Boundary Condition</b>: We will face the operator $$\frac{1}{r^2}\partial_r$$. Hence, the origin is become singular and the error will turn large near origin.

  Hence, the aim of my thesis is contained the following topic,

   1. Confirms the simulative results of Choptuik and summarizes useful numerical techniques.
   2. Summarize the analysis of numerical schemes for solving spherical symmetric Einstein’s equations.
   3. A survey of the well-posed boundary condition will be introduced.

## Results

  <b>Weak Solutions</b><br>
  The amplitude $$A=0.0001$$ is chosen. As we can see, the evolution of scalar field behaves as we would expect for evolution in flat spacetime.
  <center>
  <img src="/images/projects/nr/sfweak.png" width="400" alt="diag of sf"/>
  <figcaption>Figure: Weak scalar fields</figcaption>
  </center>
  Besides, Figure shows the value of the lapse function $$\alpha$$ at origin drop to near 0.6 when the incoming pulse reaches the origin. However, since the scaler field is not large enough to collapse to a black hole, the value of $$\alpha$$ at origin finally returns to 1.
  <center class="half">
    <img src="/images/projects/nr/wa.png" width="300" alt="ori img"/><img src="/images/projects/nr/walpha.png" width="300" alt="overfit label"/> 
    <figcaption>Figure: The left hand side subfigure is "a" and the right hand side subfigure is "alpha".</figcaption>
  </center>
  <b>Strong Solutions</b><br>
  The strong scalar field with amplitude $$A = 0.002$$ is implemented below. The scalar field is presented in as following figure. The significant phenomenon can be observed that the scalar field is "freezing" near origin.
  <center>
    <img src="/images/projects/nr/sfstrong.png" width="400" alt="diag of sf"/>
    <figcaption>Figure: Strong scalar fields</figcaption>
  </center>
  The lapse function $$\alpha$$ at origin approaches to 0 as time evolves. Since the lapse is near zero in the central regions, the evolution stops near origin, freezing the scalar field.
  <center class="half">
    <img src="/images/projects/nr/sa.png" width="300" alt="ori img"/><img src="/images/projects/nr/salpha.png" width="300" alt="overfit label"/> 
    <figcaption>Figure: The left hand side subfigure is "a" and the right hand side subfigure is "alpha".</figcaption>
  </center>
  On the other hand,  ADM mass $$M_{ADM}$$ in computational domain is about 0.54. Then, the mass aspect of black hole is about 0.24 in stable region by the following figure.
  <center>
    <img src="/images/projects/nr/sBHMass.png" width="400" alt="diag of sf"/>
    <figcaption>Figure: Strong scalar fields</figcaption>
  </center>
  The fact that the mass of final black hole is half the initial ADM mass is to be expected, because the initial pulse divide by two packet: one goes inward and generate black holes and the other escapes to infinity.

## Material
  * [Slides](./../../../pdf/projects/nr/slides(v3).pdf)

  * [Algorithm](https://github.com/Singyuan/Einstein-Scalar-Field-Collapse)


## Referencess

  1. R. Arnowitt, S. Deser, C. W. Misner, <i>The Dynamics of General Relativity. Gravitation</i>, (1962).
  2. M. W. Choptuik, <i>Consistency of finite-difference solutions of Einstein equations</i>, (1991).
  3. M. W. Choptuik, <i>Universality and Scaling in Gravitational Collapse of a Massless Scalar Field</i>, (1993).

## Acknowledgements

  I sincerely thank Dr. Peming Ho and Dr. ChunHao Teng for the guidance and assistance.