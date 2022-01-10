---
layout: default
title: Catergory
---

<ul class="category"> 
  {% for category in site.categories %}
  <div class="category-item">
    <h2 id="{{category | first}}" class="{{category | first}}-tag">{{category | first}}</h2>
      {% for posts in category %}
        {% for post in posts %}
          {% if post.url %}
          <li>
            <a class="title" href="{{ post.url | prepend: site.url }}">{{ post.title }}</a>
          </li>
          {% endif %}
        {% endfor %}
      {% endfor %}
  </div>
  {% endfor %}
</ul>