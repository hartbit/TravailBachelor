---
layout: page
title: Revues
permalink: /revues/
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

{% for revues in site.data.revues %}
<div class="row">
  <div class="column1">
    <a href="{{ revues["Lien vers le site du journal"] }}">
      <img src="{{ revues.image }}" width="150"/>
    </a>
  </div>
  <div class="column2">
    <h1><a href="{{ revues["Lien vers le site du journal"] }}">{{ revues["Revues / périodique à suivre"] }}</a></h1>
    <b>Facteur d'impact :</b> {{ revues["Facteur d'impact"] }}<br/>
    <b>Lien pour suivre :</b> <a href="{{ revues["Moyen de les suivre"] }}">{{ revues["Moyen de les suivre"] }}</a><br/>
  </div>
</div>
{% endfor %}
