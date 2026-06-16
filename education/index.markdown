---
layout: page
title: educational resources
order: 6
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
{% include_relative scripts-local.html %}
{% include styles/styles-common.css.html %}

<div class="section-header"><h4 data-i18n="edu.heading">Educational Resources</h4></div>
<p class="edu-intro" data-i18n="edu.intro">Digital tools for Francophone music and language education in K–12 schools.</p>

<div id="edu-filters">
  <div id="edu-access-tabs">
    <button class="edu-tab active" data-filter="all" data-i18n="edu.filter_all">All</button>
    <button class="edu-tab" data-filter="free" data-i18n="edu.filter_free">Free</button>
    <button class="edu-tab" data-filter="subscription" data-i18n="edu.filter_sub">Subscription</button>
  </div>
  <div id="edu-category-tabs">
    <button class="edu-cat active" data-cat="all" data-i18n="edu.cat_all">All categories</button>
    <button class="edu-cat" data-cat="music" data-i18n="edu.cat_music">Music creation</button>
    <button class="edu-cat" data-cat="language" data-i18n="edu.cat_language">Language learning</button>
    <button class="edu-cat" data-cat="curriculum" data-i18n="edu.cat_curriculum">Curriculum</button>
  </div>
</div>

<div id="edu-count"></div>
<div id="edu-grid"></div>
