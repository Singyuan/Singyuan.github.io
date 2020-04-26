---
layout: single
permalink: /projects/IBM/Data_Parallelism_ML.html
excerpt: This project cooperates with Dr. Andrew Rosenberg, Dr. Minghung Chen, Dr. Ihsin Chung, and Dr. Weichung Wang
header:
  overlay_image: /images/projects/subheads.jpg
  overlay_filter: 0.5
title: "Analysis of Data Parallelism Acceleration on Speech Recognition and Synthesis ML Algorithms"
author_profile: true
comments: true
---

## Introduction

  The purpose is to accelerate the speech algorithm by parallelism using multiple GPUs. The algorithm given by speech group in IBM Thomas J. research center is about converting the word to spectrum, including
  three models: (i) encoder, (ii) decoder and (iii) post process, as shown in following figure.

  <center>
    <img src="/images/projects/para_ai/structure.png" width="550" alt="structure"/>
    <figcaption>Figure: Structure of speech algorithm.</figcaption>
  </center>

## Goal
  This study accelerated the speech algorithm by data parallelism. The analysis discusses some challenges and how they are addressed. The following is research method:

  1. <b>Data Parallelism</b>: Add data parallelism, maximize the GPUs utilization and find the bottleneck which reduced the utilization of GPUs.

  2. <b>Analysis</b>: Analyze each function and accelerate it further and find the bottleneck function.

## Results
  * The function ''trainloader'' block the communication between CPU and GPUs.
    <center class="half">
      <img src="/images/projects/para_ai/utilization_2gpu_notl.png" width="300" alt="without"/><img src="/images/projects/para_ai/utilization_2gpu_tl.png" width="300" alt="with"/> 
      <figcaption>Figure: Comparison with and without function ''trainloader''.</figcaption>
    </center>
    By the way, The function ''trainloader'' is to sort the data before generation.

  * In order to verify the bottleneck, observe the performance without the function ''trainloader'', when using more GPUs. As shown in following figure, utilization of one GPU is improved when we use more GPUs.
    <center>
      <img src="/images/projects/para_ai/utilization_gpus.png" width="400" alt="structure"/>
      <figcaption>Figure: Comparison utilization of one GPU in different number of GPUs.</figcaption>
    </center>

  * Removing the function ''trainloader'', observe the performance of each function. The following figure shows the relation between the GPU utilization and the training time taken in each function. The performance is improved, except for function ''decoder'' and ''postproc''.
    <center>
      <img src="/images/projects/para_ai/comparison22.png" width="400" alt="structure"/>
      <figcaption>Figure: Comparison each function in different number of GPUs.</figcaption>
    </center>



## References
  1. A. Rosenberg, A. Sethy, B. Ramabhadran and M. Picheny, <i>End-to-end Speech Recognition and keywords search on low resource language.</i>

## Material

  [Poster](./../../../pdf/projects/IBM/Data_Parallelism.pdf)


## Acknowledgements

  I sincerely thank my advisor Dr. Rosenberg, Dr. Chung and Dr. Chen for the guidance and encouragement. Also, I would like to thank Dr. Wang for this intern opportunity at IBM Research.