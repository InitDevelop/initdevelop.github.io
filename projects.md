---
layout: default
title: Projects
---

<h1 class="page-title">Projects</h1>

<div class="posts-grid">
  {% assign projects = site.posts | where: "category", "project" %}
  {% for post in projects %}
    <a href="{{ post.url | relative_url }}" class="post-card {% if post.image %}has-image{% else %}no-image{% endif %}">
      
      {% if post.image %}
        <div class="card-image">
          <img src="{{ post.image | relative_url }}" alt="{{ post.title }}">
        </div>
      {% endif %}

      <div class="card-content">
        <h3>{{ post.title }}</h3>
        
        {% unless post.image %}
          <p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% endunless %}
        
        <span class="read-more">View Project &rarr;</span>
      </div>
      
    </a>
  {% endfor %}
</div>