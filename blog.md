---
layout: default
title: Blog
---

# Blog Posts

<div class="blog-container">
{% for blog in site.data.blogs %}
<div class="blog-post">
  <h2 class="blog-title">
    <a href="{{ blog.link }}" target="_blank" rel="noopener">{{ blog.title }}</a>
  </h2>
  <div class="blog-meta">
    <span class="blog-author">By {{ blog.author }}</span>
    <span class="blog-date">{{ blog.date | date: "%B %d, %Y" }}</span>
  </div>
  <p class="blog-excerpt">{{ blog.excerpt }}</p>
  <a href="{{ blog.link }}" class="blog-link" target="_blank" rel="noopener">Read more →</a>
</div>
{% endfor %}
</div>
