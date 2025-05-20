
---
layout: default
title: Blog
permalink: /blog/
---

<h1>Fusion News Blog</h1>
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
