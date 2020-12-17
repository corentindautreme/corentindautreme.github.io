---
layout: page
title: Projects
permalink: /projects/
---

{% for project in site.projects | reversed %}
<div class="post">
    <h2>{{ project.name }}</h2>
    <a href="{{ project.preview }}" class="project-preview"><img src="{{ project.preview }}" /></a>
    <div class="project-info">
        <p>{{ project.content | markdownify }}</p>
        <p style="margin-top: 0.5em;">
            {% assign labels = project.labels | split: ", " %}
            {% for label in labels %}
            <div class="project-label">{{ label }}</div>
            {% endfor %}
        </p>
    </div>
</div>
{% endfor %}