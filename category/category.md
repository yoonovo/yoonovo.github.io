---
layout: default
title: category
---
<ul class="category">
  {% for category in site.categories %}
  <h2 id="{{category | first}}">{{category | first}}</h2>
  {% for posts in category %}
  {% for post in posts %}
  {% if post.url %}
  <li>
    <a class="title" href="{{ post.url | prepend: site.url }}">{{ post.title }}</a>
  </li>
  {% endif %}
  {% endfor %}
  {% endfor %}
  {% endfor %}
</ul>