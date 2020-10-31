---
layout: page
title: Projects
permalink: /projects/
---

{% for project in site.projects %}
  <h2>{{ project.name }}</h2>
  <p>{{ project.content | markdownify }}</p>
{% endfor %}