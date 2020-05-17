---
layout: page
title: Ouvrages
permalink: /ouvrages/
---

{% for ouvrage in site.data.ouvrages %}
  {% capture content %}
    <b>Auteur :</b> {{ ouvrage.auteur }}<br/>
    <b>Date de publication :</b> {{ ouvrage.date_publication }}<br/>
  {% endcapture %}
  
  {% include image_item.html link=ouvrage.lien image=ouvrage.image title=ouvrage.titre content=content %}
{% endfor %}
