---
layout: page
title: sing along
nav_exclude: true
---

<script async src="https://www.googletagmanager.com/gtag/js?id=G-38882FHV3H"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-38882FHV3H');
</script>

{% include_relative styles-local.html %}
{% include styles/styles-common.css.html %}

<!-- ── Grid view ───────────────────────────────────────────────────────── -->
<div id="sing-grid-view">

  <div class="sing-hero">
    <div class="sing-hero-icon">🎵</div>
    <h2 class="sing-hero-title">Chantons ensemble!</h2>
    <p class="sing-hero-sub">Choose a song — <em>Choisissez une chanson</em></p>
  </div>

  <div class="sing-toolbar">
    <input type="search" id="sing-search" class="sing-search" placeholder="Search / Rechercher…" oninput="filterSongs()">
    <button class="sing-btn surprise-btn" onclick="pickRandom()">🎲 Surprise!</button>
  </div>

  <div id="sing-count" class="sing-count"></div>
  <div id="sing-grid" class="sing-grid"></div>

</div>

<!-- ── Stage view ──────────────────────────────────────────────────────── -->
<div id="sing-stage" class="hidden">

  <div class="stage-nav">
    <button class="sing-btn back-btn" onclick="showGrid()">← All songs</button>
    <div class="stage-arrows">
      <button id="stage-prev" class="sing-btn arrow-btn" onclick="prevSong()" aria-label="Previous song">‹</button>
      <button id="stage-next" class="sing-btn arrow-btn" onclick="nextSong()" aria-label="Next song">›</button>
    </div>
  </div>

  <div class="stage-info">
    <div id="stage-title" class="stage-title"></div>
    <div id="stage-comp" class="stage-comp"></div>
  </div>

  <div class="stage-player">
    <button id="stage-play-btn" class="play-btn" onclick="togglePlay()" disabled aria-label="Play">▶</button>
    <div id="kp-progress" class="kp-progress"><div id="kp-progress-fill" class="kp-progress-fill"></div></div>
    <div class="tempo-row">
      <button class="tempo-btn" data-scale="0.5"  onclick="setTempoScale(0.5)"  title="Slow">🐢</button>
      <button class="tempo-btn active" data-scale="1"  onclick="setTempoScale(1)"    title="Normal">♩</button>
      <button class="tempo-btn" data-scale="1.5"  onclick="setTempoScale(1.5)"  title="Fast">🐇</button>
    </div>
  </div>

  <div id="stage-lyrics" class="stage-lyrics"></div>

  <!-- Hidden KernPlayer DOM hooks -->
  <div id="audiobutton-container" style="position:absolute;width:0;height:0;overflow:hidden;opacity:0;pointer-events:none;">
    <span id="audiobutton-play"></span>
  </div>

</div>

{% include scripts/kern-player.html %}
{% include_relative scripts-local.html %}
