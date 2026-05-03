---
layout: default
title: Blog Posts
permalink: /blog/
---

<h1>Latest Blog Posts</h1>

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
    <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
    <a href="{{ post.url }}">Read More &rarr;</a>
  </li>
  {% endfor %}
</ul>