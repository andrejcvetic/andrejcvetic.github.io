---
layout: page
permalink: /publications/
title: publications
description:
nav: false
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="pub-category">Articles</h2>
{% bibliography --query @article[keywords=article] %}

<h2 class="pub-category">Chapters</h2>
{% bibliography --query @incollection %}

<h2 class="pub-category">Book Reviews</h2>
{% bibliography --query @article[keywords=review] %}

</div>
