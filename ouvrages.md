---
layout: page
title: Ouvrages
permalink: /ouvrages/
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

{% for ouvrage in site.data.ouvrages %}
<div class="row">
  <div class="column1">
    <a href="{{ ouvrage.Lien }}">
      <img src="{{ ouvrage.Image }}" width="150"/>
    </a>
  </div>
  <div class="column2">
    <h1><a href="{{ ouvrage.Lien }}">{{ ouvrage.Titre }}</a></h1>
    <b>Auteur :</b> {{ ouvrage.Auteur }}<br/>
    <b>Date de publication :</b> {{ ouvrage["Date publication"] }}<br/>
  </div>
</div>
{% endfor %}
