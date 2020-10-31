---
layout: page
title: Side Projects
permalink: /side-projects/
---

{% for project in site.side_projects %}
  <h2>{{ project.name }}</h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}