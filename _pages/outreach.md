---
layout: page
title: outreach
permalink: /outreach/
nav: true
nav_order: 5
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

.outreach-table {
  width: 100%;
  border-collapse: collapse;
}

.outreach-table td {
  padding: 0.4rem 0.5rem;
  vertical-align: top;
}

.outreach-table td:last-child {
  text-align: right;
  white-space: nowrap;
  color: var(--global-text-color-light);
}
</style>

<div class="tab-buttons">
  <button class="tab-btn active" onclick="showTab('conferences', this)">Conferences</button>
  <button class="tab-btn" onclick="showTab('workshops', this)">Workshops & Invited Talks</button>
  <button class="tab-btn" onclick="showTab('media', this)">Media & Public Engagement</button>
</div>

<div id="conferences" class="tab-content active">
  <p><em>* scheduled; † declined</em></p>
  <table class="outreach-table">
    <tr><td>European Political Science Society (EPSS)</td><td>2026*</td></tr>
    <tr><td>European Political Science Association (EPSA)<br><em>How does legitimising radical right influence Muslim immigrants in Germany? A research agenda</em></td><td>2024</td></tr>
    <tr><td>UK Political Psychology (UK PolPsy)<br><em>How does legitimising radical right influence Muslim immigrants in Germany? A research agenda</em></td><td>2024</td></tr>
    <tr><td>German Political Psychology Network (24hPolPsy)<br><em>Host(ile) Country: Do Immigrants React to Electoral Support for the Far-right in Germany?</em><br><em>Social Trust among Muslim Immigrants: Evidence from an experimental design</em></td><td>2024</td></tr>
    <tr><td>Politicologenetmaal<br><em>Discrimination that matters? Replication of "Perceived Discrimination and Political Behaviour" (BJPS, 2020)</em></td><td>2024</td></tr>
  </table>
</div>

<div id="workshops" class="tab-content">
  <p><em>* scheduled; † declined</em></p>
  <table class="outreach-table">
    <tr><td>Politics and Mental Health in Times of Societal Threat: Wicked or Not?, University of Amsterdam (March)</td><td>2026†</td></tr>
    <tr><td>Migration, Asylum, and Human Security in Europe, University of Southampton (June)</td><td>2026*</td></tr>
    <tr><td>Research Workshop on Political Trust, Pompeu Fabra University (October)</td><td>2026*</td></tr>
    <tr><td>COMPAS Work in Progress Series, University of Oxford (May)<br><em>Discrimination that matters? Replication of "Perceived Discrimination and Political Behaviour" (BJPS, 2020)</em></td><td>2024</td></tr>
    <tr><td>CESS Colloquium, Nuffield College, University of Oxford (February)<br><em>The Effect of Electoral Support for Far-right on Institutional and Social Trust among Muslim Immigrants: Evidence from Germany</em></td><td>2024</td></tr>
    <tr><td>Replication Webinar Series, Young Scholars Initiative (November)<br><em>In What Direction? Replication and Extension of Oskooii 2020 "Perceived Discrimination and Political Behavior"</em></td><td>2022</td></tr>
  </table>
</div>

<div id="media" class="tab-content">
  <table class="outreach-table">
    <tr><td><a href="https://www.youtube.com/shorts/ZUcHyi1tj-g" target="_blank">Young Scholars Initiative Fresh Takes</a></td><td>2025</td></tr>
  </table>
</div>

<script>
function showTab(tabId, btn) {
  document.querySelectorAll('.tab-content').forEach(el => el.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(el => el.classList.remove('active'));
  document.getElementById(tabId).classList.add('active');
  btn.classList.add('active');
}
</script>
