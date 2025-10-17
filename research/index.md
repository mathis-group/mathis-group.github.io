---
title: Research
nav:
  order: 1
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

{% assign featured_projects = site.data.projects | where: "group", "featured" %}
{% for project in featured_projects %}
  {% include project-focus.html project=project %}
{% endfor %}

{% include section.html %}


# Highlighted Publications

{% include citation.html lookup="Self-organization in computation and chemistry: Return to AlChemy" style="rich" %}

{% include citation.html lookup="Life detection in a universe of false positives" style="rich" %}

{% include citation.html lookup="Identifying molecules as biosignatures with assembly theory and mass spectrometry" style="rich" %}

{% include section.html %}

# All Publications

{% include search-box.html %}

{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" %}
