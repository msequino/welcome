---
layout: default
title: Projects
permalink: /projects/
---

# Projects

A collection of projects I've worked on, spanning distributed systems, streaming data, and creative coding.

<div class="projects-grid">
    {% for project in site.projects %}
    <div class="project-card">
        <h3 class="project-title">
            <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
        </h3>
        <p class="project-desc">{{ project.subtitle }}</p>
        <div class="project-tech">
            {% for tech in project.tech %}
            <span class="tech-badge">{{ tech }}</span>
            {% endfor %}
        </div>
    </div>
    {% endfor %}
</div>
