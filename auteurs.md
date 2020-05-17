---
layout: page
title: Auteurs
permalink: /auteurs/
---

{% for auteur in site.data.auteurs %}
  {% capture content %}
    {% if auteur.article_plus_cite %}
      <b>Article le plus cité :</b> {{ auteur.article_plus_cite }}<br/>
    {% endif %}
    <b>Date de dernière publication :</b> {{ auteur.annee_derniere_publication }}<br/>
  {% endcapture %}
  
  {% include image_item.html link=auteur.lien image=auteur.image title=auteur.nom content=content %}
{% endfor %}
