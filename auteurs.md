---
layout: page
title: Auteurs
permalink: /auteurs/
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

{% for auteur in site.data.auteurs %}
<div class="row">
  <div class="column1">
    <a href="{{ auteur.Lien }}">
      <img src="{{ auteur.Image }}" width="150"/>
    </a>
  </div>
  <div class="column2">
    <h1><a href="{{ auteur.Lien }}">{{ auteur.Nom }}</a></h1>
    <b>Article le plus cité :</b> {{ auteur["Article le plus cité"] }}<br/>
    <b>Dernières publications :</b> {{ auteur["Dernières publications"] }}<br/>
  </div>
</div>
{% endfor %}
