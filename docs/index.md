---
layout: default
title: Home
permalink: /
---

<section class="hero">
    <h1 class="hero-title">Scalable Systems & Creative Code</h1>
    <p class="hero-subtitle">Curious engineer focused on distributed systems, streaming data pipelines, and elegant solutions to complex problems.</p>
    <div>
        <a href="{{ '/about' | relative_url }}" class="btn btn-primary">Learn About Me</a>
        <a href="{{ '/projects' | relative_url }}" class="btn btn-secondary">View Projects</a>
    </div>
</section>

<section class="section">
    <h2 class="section-title">Featured Projects</h2>
    <div class="projects-grid">
        {% for project in site.projects limit: 3 %}
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
    <div style="text-align: center; margin-top: 2rem;">
        <a href="{{ '/projects' | relative_url }}" class="btn btn-primary">View All Projects</a>
    </div>
</section>

<section class="section">
    <h2 class="section-title">Core Skills</h2>
    <div class="skills-container">
        <div class="skill-category">
            <h3 class="skill-title">Backend & Infra</h3>
            <ul class="skill-list">
                <li>Distributed Systems</li>
                <li>Streaming Data Pipelines</li>
                <li>Microservices Architecture</li>
                <li>Cloud Infrastructure (AWS)</li>
                <li>Kubernetes & Docker</li>
            </ul>
        </div>
        <div class="skill-category">
            <h3 class="skill-title">Languages & Tools</h3>
            <ul class="skill-list">
                <li>Python, Go, Rust</li>
                <li>Java, TypeScript</li>
                <li>Apache Kafka, Apache Spark</li>
                <li>PostgreSQL, Redis</li>
                <li>Git, CI/CD</li>
            </ul>
        </div>
        <div class="skill-category">
            <h3 class="skill-title">Interests</h3>
            <ul class="skill-list">
                <li>Game Development</li>
                <li>Raspberry Pi Projects</li>
                <li>Open Source Contribution</li>
                <li>Technical Writing</li>
                <li>System Design</li>
            </ul>
        </div>
    </div>
</section>

<section class="section">
    <h2 class="section-title">Latest Articles</h2>
    <div class="blog-feed">
        {% for post in site.posts limit: 3 %}
        <article class="post-preview">
            <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">
                {{ post.date | date: "%B %d, %Y" }}
            </time>
            <h3 class="post-title">
                <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h3>
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 200 }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
        </article>
        {% endfor %}
    </div>
    <div style="text-align: center; margin-top: 2rem;">
        <a href="{{ '/blog' | relative_url }}" class="btn btn-primary">All Articles</a>
    </div>
</section>

<!--section class="section text-center">
    <h2 class="section-title">Let's Work Together</h2>
    <p>Interested in collaboration or just want to chat? Feel free to reach out.</p>
    <a href="{{ '/contact' | relative_url }}" class="btn btn-primary">Get In Touch</a>
</section-->
