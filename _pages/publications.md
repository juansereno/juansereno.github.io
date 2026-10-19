---
layout: page
permalink: /publications/
title: publications
description: A full, automatically updated list is also on my <a href='https://scholar.google.com/citations?user=KMzVSbMAAAAJ&hl=en'>Google Scholar profile</a>.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Journal articles</h2>
{% bibliography --group_by none --query @article %}

<h2 class="bibliography">Book chapters</h2>
{% bibliography --group_by none --query @incollection %}

<h2 class="bibliography">Conference papers</h2>
{% bibliography --group_by none --query @inproceedings %}

</div>
