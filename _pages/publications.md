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

<div class="publications">

<h2 class="bibliography">Articles</h2>
{% bibliography --query @article[keywords=article] %}

<h2 class="bibliography">Chapters</h2>
{% bibliography --query @incollection %}

<h2 class="bibliography">Reviews</h2>
{% bibliography --query @article[keywords=review] %}

</div>
