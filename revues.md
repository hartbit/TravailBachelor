---
layout: page
title: Revues
permalink: /revues/
---

{% for revue in site.data.revues %}
  {% capture content %}
    <b>Facteur d'impact :</b> {{ revue.facteur_impact }}<br/>
    <a href="{{ revue.lien_suivre }}">Lien pour suivre</a><br/>
  {% endcapture %}
  
  {% include image_item.html link=revue.lien_journal image=revue.image title=revue.nom content=content %}
{% endfor %}
