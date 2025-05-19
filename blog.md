---
layout: default
title: Blog
---

# Blog

{% for post in site.posts %}
  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p class="meta">
      <strong>Published:</strong> {{ post.date | date: "%B %d, %Y %I:%M %p" }}<br>
      <strong>Author:</strong> {{ post.author }}<br>
      {{ post.note }}<br>
      {{ post.collaboration }}
    </p>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}
