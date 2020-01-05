---
layout: page
title: About
---

<p>Posts in category "philosophy" are:</p>

<ul>
  {% for post in site.categories.philosophy %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
</ul>

