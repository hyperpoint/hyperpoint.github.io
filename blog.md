---
layout: default
title: Blog
---

# Blog

{% for post in paginator.posts %}
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

<!-- Pagination links -->
{% if paginator.total_pages > 1 %}
  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path }}">Previous</a>
    {% endif %}
    {% for page in (1..paginator.total_pages) %}
      {% if page == paginator.page %}
        <span>{{ page }}</span>
      {% else %}
        <a href="{{ site.paginate_path | replace: ':num', page }}">{{ page }}</a>
      {% endif %}
    {% endfor %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path }}">Next</a>
    {% endif %}
  </div>
{% endif %}
