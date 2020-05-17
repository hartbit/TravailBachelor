---
layout: page
title: Articles
permalink: /articles/
---

{% for article in site.data.articles %}
## [{{ article.Titre }}]({{ article.Lien }})

* **Auteur :** {{ article.Auteur }}
* **Date :** {{ article.Date }}
* **Nombre de citations :** {{ article["Nombre de citations"] }}
* **Journal :** {{ article.Journal }}
* **Référence :** {{ article["Référence"] }}
{% endfor %}
