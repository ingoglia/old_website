---
layout: page
title: About
---


<ul>
  {% for post in site.categories.art %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

