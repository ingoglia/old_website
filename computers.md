---
layout: page
title: Computers 
---

<ul>
  {% for post in site.categories.computers %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

