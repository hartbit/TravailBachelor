---
layout: page
title: LinkedIn
permalink: /linkedin/
---

<h1>Entreprises</h1>

{% include linkedin_accounts.html accounts=site.data.linkedin_entreprises %}

<h1>Associations</h1>

{% include linkedin_accounts.html accounts=site.data.linkedin_associations %}

<h1>Groupes</h1>

{% for account in site.data.linkedin_groupes %}
  {% capture image %}
  ../assets/images/{{ account.nom | slugify }}.png
  {% endcapture %}

  {% capture content %}
  <b>Nombre d'abonnés :</b> {{ account.nombre_abonnes }}
  <p>{{ account.description }}</p>
  {% endcapture %}

  {% include image_item.html link=account.lien_linkedin image=image title=account.nom content=content %}
{% endfor %}

<h1>Personnes</h1>

{% include linkedin_accounts.html accounts=site.data.linkedin_personnes %}

http://127.0.0.1:4000/MandatVeille/assets/images/Lean%20Six%20Sigma.jpg
