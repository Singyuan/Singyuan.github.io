---
layout: single
title: "About"
author_profile: true
permalink: /
---

I am an Assistant Professor in the Department of Mathematics at National Central University. My research lies at the intersection of manifold learning, machine learning, and applied mathematics, with particular interests in spectral methods, kernel methods, and learning theory.

## Research Interests

### Manifold Learning and Spectral Methods

I develop geometric and computational methods for complex data, including diffusion maps, vector diffusion maps, multimodal learning, and scalable landmark methods.

### Machine Learning and Kernel Methods

I study statistical and theoretical aspects of machine learning, including kernel-based reinforcement learning, sample complexity, and uncertainty in data-driven models.

## International Research Experiences

- **Technion – Israel Institute of Technology**, Haifa, Israel · December 2025–June 2026  
  Research Visitor
- **IBM Thomas J. Watson Research Center**, New York, U.S. · July–August 2018  
  Overseas Internship Program (Ministry of Education)

## Industry Internship Experiences

- **Delta Electronics – Delta Smart Manufacturing R&D Center** · August–October 2024  
  Research Engineer Intern / Intelligent Process Automation for HSK Insertion
- **MediaTek Research** · July–October 2022  
  Research Scientist Intern / Sample Complexity of Kernel-Based Q-Learning

## Education

- **Ph.D. in Data Science**, National Taiwan University and Academia Sinica · 2026
- **M.S. in Applied Mathematical Sciences**, National Taiwan University · 2020
- **B.S. in Applied Mathematics**, National Chiao Tung University · 2017

## Publications

{% assign publications = site.data.publications | sort: "year" | reverse %}
{% for publication in publications %}
{% include publication-citation.html publication=publication number=forloop.index %}
{% endfor %}

[Publication details and additional links →]({{ '/publications/' | relative_url }})

## Honors and Awards

- **Excellent Research Award**, Taiwan-Japan Joint Workshop for Young Scholars in Applied Mathematics · 2025
- **MATLAB & Simulink Call for Papers Merit Award**, TeraSoft & MathWorks · 2024
- **TiC100 Entrepreneurial Action Award**, Taiwan Social Enterprise Innovation and Entrepreneurship Society · 2024
- **Yunus Prize**, 8th Social Innovation and Entrepreneurship Competition, National Central University · 2023
- **College Student Research Creativity Award**, Ministry of Science and Technology · 2016

## Invited Talks and Presentations

- The 10th Computational Mathematics & Scientific Computing for Young Researchers · August 2026
- The 26th Conference of the International Linear Algebra Society · June 2025
- The 15th Taiwan-Japan Joint Workshop for Young Scholars in Applied Mathematics · March 2025
- NSTC-NCTS-SPEC Joint Conference on Interdisciplinary Research · April 2024
- Meet Physicians, Mathematicians and Statisticians · March 2022
