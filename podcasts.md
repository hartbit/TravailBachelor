---
layout: page
title: Podcasts
permalink: /podcasts/
---

<style>
.row {
  display: flex;
  margin-bottom: 30px;
}

.column1 {
  flex: 25%;
}

.column2 {
  flex: 75%;
}
</style>

{% for podcast in site.data.podcasts %}
<div class="row">
  <div class="column1">
    <a href="{{ podcast.Lien }}">
      <img src="{{ podcast.Image }}" width="150" height="150"/>
    </a>
  </div>
  <div class="column2">
    <b>Titre :</b> {{ podcast.Titre }}<br/>
    <b>Auteur :</b> {{ podcast.Auteur }}<br/>
    <b>Résumé :</b> {{ podcast["Résumé"] }}
  </div>
</div>
{% endfor %}
