---
layout: page
title: Blogs
permalink: /blogs/
---

{% for blog in site.data.blogs %}
  {% capture content %}
    <p>{{ blog.presentation }}</p>
    {% if blog.nom == "Forbes Leadership" %}
      {% include blog_articles.html articles=site.data.blogs_forbes %}
    {% elsif blog.nom == "PROSCI (Blog)" %}
      {% include blog_articles.html articles=site.data.blogs_prosci %}
    {% endif %}
  {% endcapture %}
  
  {% include image_item.html link=blog.lien image=blog.image title=blog.nom content=content %}
{% endfor %}
