---
layout: default
title: Blog
permalink: /blog/
---

<div class="blog-container">
  <h1>Fusion News Blog</h1>
  <ul class="post-list">
    {% assign seen_titles = "" | split: "," %}
    {% for post in site.posts %}
      {% assign title = post.title | strip %}
      {% unless seen_titles contains title %}
        <li>
          <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
          <p class="post-meta">Published: {{ post.date | date: "%B %d, %Y %I:%M %p" }}</p>
        </li>
        {% assign seen_titles = seen_titles | push: title %}
      {% endunless %}
    {% endfor %}
  </ul>
</div>
