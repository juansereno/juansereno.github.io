---
layout: page
title: research
permalink: /research/
description: My work sits between control theory and mathematical biology. The common thread is building models that are faithful enough to be useful clinically, and control and estimation methods that remain tractable when those models are switched, nonlinear and only partially measured.
nav: true
nav_order: 1
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% assign sorted_projects = site.projects | sort: "importance" %}
<div class="row row-cols-1 row-cols-md-2">
{% for project in sorted_projects %}
  {% include projects.liquid %}
{% endfor %}
</div>
</div>
