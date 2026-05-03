---
layout: default
title: Life
permalink: /life/
---

<h1 style="margin-bottom: 40px;">Life</h1>

<div class="posts-grid">
  {% for post in site.posts %}
    {% if post.category == 'life' %}
      <a href="{{ post.url }}" class="post-card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        <span style="font-size: 0.9rem; color: #888;">Read More &rarr;</span>
      </a>
    {% endif %}
  {% endfor %}
</div>