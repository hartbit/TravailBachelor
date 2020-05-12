---
layout: page
title: YouTube
permalink: /youtube/
---

{% for video in site.data.youtube %}
## {{ video.Titre }}

* **Date :** {{ video.Date }}
* **Nombre de vues :** {{ video["Nb de vue"] }}

<iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/{{ video["Code de la vidéo"] }}"
    frameborder="0"
    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
>
</iframe>
<br/>
{% endfor %}
