---
layout: home
title: "Latest Science Summaries"
header:
  overlay_image: "/assets/images/banner.jpg"
pagination:
  enabled: true
---

<div class="news-container">
  {% for post in paginator.posts %}
    <article class="news-item">
      {% if post.featured_image %}
        <img src="{{ post.featured_image }}" alt="{{ post.title }}">
      {% endif %}
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </article>
  {% endfor %}
</div>

<!-- Pagination -->
<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}" class="prev">« Previous</a>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}" class="next">Next »</a>
  {% endif %}
</div>
