---
layout: page
title: Activités
permalink: /activites/
---

<div id="toc_container">
  <p class="toc_title">Table des matières</p>
  <ul class="toc_list">
    <li><a href="#court">1. Temps de conception court</a></li>
    <li><a href="#moyen">2. Temps de conception moyen</a></li>
    <li><a href="#long">3. Temps de conception long</a></li>
  </ul>
</div>

<h2 id="court">1. Temps de conception court</h2>

{% for outil in site.data.court %}
  {% include outil.html outil=outil %}
{% endfor %}

<h2 id="moyen">2. Temps de conception moyen</h2>

{% for outil in site.data.moyen %}
  {% include outil.html outil=outil %}
{% endfor %}

<h2 id="long">3. Temps de conception long</h2>

{% for outil in site.data.long %}
  {% include outil.html outil=outil %}
{% endfor %}
