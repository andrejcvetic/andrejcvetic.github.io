---
layout: page
title: outreach
permalink: /outreach/
nav: true
nav_order: 3
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

.talk-cards {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
}

.talk-card {
  border: 1px solid var(--global-divider-color);
  border-radius: 6px;
  padding: 1rem 1.1rem;
  background: var(--global-bg-color);
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
}

.talk-card .talk-badge {
  display: inline-block;
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--global-theme-color);
  margin-bottom: 0.1rem;
}

.talk-card .talk-title {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--global-text-color);
  flex-grow: 1;
}

.talk-card .talk-meta {
  font-size: 0.82rem;
  color: var(--global-text-color-light);
}

.talk-card .talk-link a {
  font-size: 0.85rem;
}
</style>

<div class="tab-buttons">
  <button class="tab-btn active" onclick="showTab('conferences', this)">Conferences</button>
  <button class="tab-btn" onclick="showTab('workshops', this)">Workshops & Invited Talks</button>
  <button class="tab-btn" onclick="showTab('media', this)">Media & Public Engagement</button>
</div>

<div id="conferences" class="tab-content active">
  <div class="talk-cards">

    <div class="talk-card">
      <div class="talk-badge">Upcoming</div>
      <div class="talk-title">Autocratic Booms and Democratic Echoes: State Repression and Democratic Aspirations in Hybrid Regimes</div>
      <div class="talk-meta">European Political Science Society (EPSS) · Belfast · June 2026</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">How does legitimising radical right influence Muslim immigrants in Germany? A research agenda</div>
      <div class="talk-meta">European Political Science Association (EPSA) · Cologne · July 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">How does legitimising radical right influence Muslim immigrants in Germany? A research agenda</div>
      <div class="talk-meta">UK Political Psychology (UK PolPsy) · Southampton · June 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">Host(ile) Country: Do Immigrants React to Electoral Support for the Far-right in Germany?</div>
      <div class="talk-meta">German Political Psychology Network (24hPolPsy) · Vienna · September 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">Social Trust among Muslim Immigrants: Evidence from an experimental design</div>
      <div class="talk-meta">German Political Psychology Network (24hPolPsy) · Vienna · September 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">Discrimination that matters? Replication of "Perceived Discrimination and Political Behaviour" (BJPS, 2020)</div>
      <div class="talk-meta">Politicologenetmaal · Maastricht · June 2024</div>
    </div>

  </div>
</div>

<div id="workshops" class="tab-content">
  <div class="talk-cards">

    <div class="talk-card">
      <div class="talk-badge">Upcoming</div>
      <div class="talk-title">It's Not Where They Come From, but What They Bring with Themselves: Gender Expression, Sexuality, and Disability in Attitudes towards Asylum Seekers</div>
      <div class="talk-meta">Migration, Asylum, and Human Security in Europe · University of Southampton, UK · 23 June 2026</div>
    </div>

    <div class="talk-card">
      <div class="talk-badge">Upcoming</div>
      <div class="talk-title">In the System We Trust! Electoral Support for the Populist Right and Political Trust Among Immigrants in Western Europe</div>
      <div class="talk-meta">Research Workshop on Political Trust · Pompeu Fabra University, Barcelona · 14–16 October 2026</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">When Normalisation Comes at No Cost? Legitimisation of the Populist Right and Mental Health of Immigrants</div>
      <div class="talk-meta">Politics and Mental Health in Times of Societal Threat: Wicked or Not? · University of Amsterdam, Netherlands · March 2026</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">Discrimination that matters? Replication of "Perceived Discrimination and Political Behaviour" (BJPS, 2020)</div>
      <div class="talk-meta">COMPAS Work in Progress Series · University of Oxford, UK · May 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">The Effect of Electoral Support for Far-right on Institutional and Social Trust among Muslim Immigrants: Evidence from Germany</div>
      <div class="talk-meta">CESS Colloquium · Nuffield College, University of Oxford, UK · February 2024</div>
    </div>

    <div class="talk-card">
      <div class="talk-title">In What Direction? Replication and Extension of Oskooii 2020 "Perceived Discrimination and Political Behavior"</div>
      <div class="talk-meta">Replication Webinar Series · Young Scholars Initiative · November 2022</div>
    </div>

  </div>
</div>

<div id="media" class="tab-content">
  <div class="talk-cards">

    <div class="talk-card">
      <div class="talk-badge">Interview</div>
      <div class="talk-title"><a href="https://www.youtube.com/shorts/ZUcHyi1tj-g" target="_blank">Young Scholars Initiative Fresh Takes</a></div>
      <div class="talk-meta">Young Scholars Initiative · Online · 2025</div>
    </div>

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
