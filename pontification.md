---
layout: page
title: About
---

<p>Posts in category "pontification" are:</p>

<ul>
  {% for post in site.categories.pontification %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

