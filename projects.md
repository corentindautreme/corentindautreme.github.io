---
layout: page
title: Projects
permalink: /projects/
---

{% for project in site.projects %}
<div class="post">
    <h2>{{ project.name }}</h2>
    <a href="{{ project.preview }}" class="project-preview"><img src="{{ project.preview }}" /></a>
    <div class="project-info">
        <p>{{ project.content | markdownify }}</p>
    </div>
</div>
{% endfor %}