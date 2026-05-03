---
layout: default
title: About & Portfolio
permalink: /about/
---

## About Me

I am a developer who loves building things using static site generators. Jekyll offers simplicity... (Detailed Bio Here)

---

## My Projects

{% assign projects = site.data.projects %}

{% for project in projects %}
<div class="project-card">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
    <a href="{{ project.link }}">View Project</a>
</div>
{% endfor %}