---
layout: page
title: Podcasts
permalink: /podcasts/
---

<style>
.row {
  display: flex;
  margin-bottom: 40px;
}

.column1 {
  flex: 25%;
}

.column2 {
  flex: 75%;
}

img {
  margin-top: 10px;
}

h1 {
  font-size: 17pt;
}
</style>

{% for podcast in site.data.podcasts %}
<div class="row">
  <div class="column1">
    <a href="{{ podcast.Lien }}">
      <img src="{{ podcast.Image }}" width="150"/>
    </a>
  </div>
  <div class="column2">
    <h1><a href="{{ podcast.Lien }}">{{ podcast.Titre }}</a></h1>
    <b>Auteur :</b> {{ podcast.Auteur }}<br/>
    <b>Résumé :</b> {{ podcast["Résumé"] }}
  </div>
</div>
{% endfor %}
