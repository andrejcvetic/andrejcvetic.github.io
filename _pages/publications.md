---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

{% include bib_search.liquid %}

<div class="publications">

{% for year in (2016..2023) reversed %}
  <h2 class="bibliography">{{ year }}</h2>

  <h3 class="bibliography">Articles</h3>
  {% bibliography --query @*[year={{ year }}, keywords=article]* --group_by none %}

  <h3 class="bibliography">Chapters</h3>
  {% bibliography --query @*[year={{ year }}, keywords=chapter]* --group_by none %}

  <h3 class="bibliography">Reviews</h3>
  {% bibliography --query @*[year={{ year }}, keywords=chapter]* --group_by none %}

{% endfor %}

</div>
