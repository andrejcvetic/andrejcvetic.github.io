---
layout: page
title: research
permalink: /research/
nav: true
nav_order: 2
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
  border-radius: 0;
  transition: all 0.2s;
  outline: none;
}

.tab-btn:hover {
  background: var(--global-hover-color);
  color: white;
}

.tab-btn.active {
  font-weight: bold;
  border-bottom: none;
  outline: none;
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

.tab-content .publications ol.bibliography {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
  margin-top: 1rem;
}

.tab-content .publications ol.bibliography li {
  border: 1px solid var(--global-divider-color);
  border-radius: 6px;
  padding: 1rem 1.1rem;
  background: var(--global-bg-color);
  margin-bottom: 0;
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}

.tab-content .publications ol.bibliography li .row {
  display: contents;
}

.tab-content .publications ol.bibliography li .title {
  font-size: 0.95rem;
  font-weight: 600;
  flex-grow: 1;
}

.tab-content .publications ol.bibliography li .author,
.tab-content .publications ol.bibliography li .periodical {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
}

.tab-content .publications ol.bibliography li .author a {
  color: var(--global-text-color) !important;
}

.tab-content .publications ol.bibliography li .links {
  margin-top: 0.3rem;
}

.tab-content .publications ol.bibliography li .pub-status-badge {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--global-theme-color);
  margin-bottom: 0.1rem;
}
</style>

<div class="tab-buttons">
  <button class="tab-btn active" onclick="showTab('articles', this)">Peer Reviewed Articles</button>
  <button class="tab-btn" onclick="showTab('underreview', this)">In Publication</button>
  <button class="tab-btn" onclick="showTab('workingpapers', this)">Working Papers</button>
  <button class="tab-btn" onclick="showTab('preregistration', this)">In Progress</button>
  <button class="tab-btn" onclick="showTab('chapters', this)">Chapters</button>
  <button class="tab-btn" onclick="showTab('reviews', this)">Reviews</button>
</div>

<div id="articles" class="tab-content active">
  <div class="publications">
    {% bibliography --query @article[keywords=article] --group_by none --sort_by year --order descending %}
  </div>
</div>

<div id="underreview" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords~=underreview] --group_by none --sort_by year --order descending %}
  </div>
</div>

<div id="workingpapers" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords=workingpaper] --group_by none --sort_by year --order descending %}
  </div>
</div>

<div id="preregistration" class="tab-content">
  <div class="publications">
    {% bibliography --query @*[keywords~=workinprogress] --group_by none --sort_by year --order descending %}
  </div>
</div>

<div id="chapters" class="tab-content">
  <div class="publications">
    {% bibliography --query @incollection --group_by none --sort_by year --order descending %}
  </div>
</div>

<div id="reviews" class="tab-content">
  <div class="publications">
    {% bibliography --query @article[keywords=review] --group_by none --sort_by year --order descending %}
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
