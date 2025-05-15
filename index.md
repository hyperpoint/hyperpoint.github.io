---
layout: default
---

Welcome to the Fusion News Blog, where we share the latest updates in fusion energy research.

## Latest Posts
{% for post in site.posts %}
  * [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
