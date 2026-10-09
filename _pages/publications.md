---
layout: single
permalink: /publications/
title: "Publications"
author_profile: true
excerpt: "Research papers and preprints."
header:
  overlay_image: /images/projects/heads.jpg
  overlay_filter: 0.5
---

{% assign journals = site.data.publications | where: "category", "journal" | sort: "year" | reverse %}
{% assign conferences = site.data.publications | where: "category", "conference" | sort: "year" | reverse %}
{% assign preprints = site.data.publications | where: "category", "preprint" | sort: "year" | reverse %}

## Journal Articles

{% for publication in journals %}
{% include publication-entry.html publication=publication %}
{% endfor %}

## Conference Papers

{% for publication in conferences %}
{% include publication-entry.html publication=publication %}
{% endfor %}

## Preprints

{% for publication in preprints %}
{% include publication-entry.html publication=publication %}
{% endfor %}
