---
layout: category
title: Posts
---

{%- if site.posts.size > 0 -%}
  <ul class="post-list-header">
    <li>
      <span class="post-idx">No.</span>
        <span class="post-category-type">Type</span>
      <h3 class="post-list-title">Title</h3>
      <span class="post-meta">Date</span>
    </li>
  </ul>
  <ul class="post-list">
    {%- for post in site.posts -%}
    <li onclick="onClickPost('{{ post.url }}')">
      <span class="post-idx">{{ forloop.rindex }}</span>
      {%- for category in post.categories -%}
        <span class="post-category-type">
          <b class="{{category}}-tag">{{ category }}</b>
        </span>
      {%- endfor -%}
      <h3 class="post-list-title">
        <a class="post-link">
          {{ post.title | escape }}
        </a>
      </h3>
      {%- assign date_format = site.minima.date_format | default: "%Y-%m-%d" -%}
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>
{%- endif -%}

<script>
function onClickPost(url){
  location.href = url;
}
</script>