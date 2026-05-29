---
layout: page
title: research2
permalink: /research2/
nav: false
---

<style>
.tab-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.5rem;
  border-bottom: 2px solid var(--global-divider-color);
  padding-bottom: 0.75rem;
}

.tab-btn {
  background: none;
  border: none;
  padding: 0.4rem 0.8rem;
  cursor: pointer;
  font-size: 0.95rem;
  color: var(--global-text-color);
  border-radius: 4px;
  transition: all 0.2s;
}

.tab-btn:hover {
  background: var(--global-hover-color);
  color: white;
}

.tab-btn.active {
  font-weight: bold;
  border-bottom: 2px solid var(--global-text-color);
}

.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
}

.tab-content .col-sm-2.abbr {
  display: none;
}

.tab-content .col-sm-8 {
  flex: 0 0 100%;
  max-width: 100%;
}
</style>

<div class="tab-buttons">
  <button class="tab-btn active" onclick="showTab('articles', this)">Peer Reviewed Articles</button>
  <button class="tab-btn" onclick="showTab('underreview', this)">Under Review</button>
  <button class="tab-btn" onclick="showTab('workingpapers', this)">Working Papers</button>
  <button class="tab-btn" onclick="showTab('preregistration', this)">Pre-registration</button>
  <button class="tab-btn" onclick="showTab('chapters', this)">Chapters</button>
  <button class="tab-btn" onclick="showTab('reviews', this)">Reviews</button>
</div>

<div id="articles" class="tab-content active">
  <div class="publications">
    {% bibliography --query @article[keywords=article] --group_by none %}
  </div>
</div>

<div id="underreview" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords~=underreview] --group_by none %}
  </div>
</div>

<div id="workingpapers" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords=workingpaper] --group_by none %}
  </div>
</div>

<div id="preregistration" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords~=workinprogress] --group_by none %}
  </div>
</div>

<div id="chapters" class="tab-content">
  <div class="publications">
    {% bibliography --query @incollection --group_by none %}
  </div>
</div>

<div id="reviews" class="tab-content">
  <div class="publications">
    {% bibliography --query @article[keywords=review] --group_by none %}
  </div>
</div>

<script>
function showTab(tabId, btn) {
  document.querySelectorAll('.tab-content').forEach(el => el.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(el => el.classList.remove('active'));
  document.getElementById(tabId).classList.add('active');
  btn.classList.add('active');
}
</script>
