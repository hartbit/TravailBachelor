---
layout: page
title: Podcasts
permalink: /podcasts/
---

{% for podcast in site.data.podcasts %}
  {% capture content %}
    <b>Auteur :</b> {{ podcast.auteur }}<br/>
    <b>Résumé :</b> {{ podcast.resume }}
  {% endcapture %}
  
  {% include image_item.html link=podcast.lien image=podcast.image title=podcast.titre content=content %}
{% endfor %}
