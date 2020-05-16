---
layout: page
title: Blogs
permalink: /blogs/
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

.post-content h2 {
  font-size: 15pt;
}
</style>

{% for blog in site.data.blogs %}
<div class="row">
  <div class="column1">
    <a href="{{ blog["Lien internet"] }}">
      <img src="{{ blog.Image }}" width="150"/>
    </a>
  </div>
  <div class="column2">
    <h1><a href="{{ blog["Lien internet"] }}">{{ blog.Nom }}</a></h1>
    <p>{{ blog["Présentation"] }}</p>
    {% if blog.Nom == "Forbes Leadership" %}
      <h2>Derniers articles publiés</h2>
      <ul>
        {% for article in site.data.blogs_forbes %}
          <li><b>{{ article.Auteur }} :</b> <a href="{{ article["Lien internet"] }}">{{ article.Nom }}</a> ({{ article.Date }})</li>
        {% endfor %}
      </ul>
    {% elsif blog.Nom == "PROSCI (Blog)" %}
      <h2>Derniers articles publiés</h2>
      <ul>
        {% for article in site.data.blogs_prosci %}
          <li><b>{{ article.Auteur }} :</b> <a href="{{ article["Lien internet"] }}">{{ article.Nom }}</a> ({{ article.Date }})</li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
</div>
{% endfor %}
