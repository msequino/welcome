---
layout: default
title: Blog
permalink: /blog/
---

# Articles

Thoughts, tutorials, and insights about software engineering, systems design, and technology.

<div class="blog-feed">
    {% for post in site.posts %}
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
