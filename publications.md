---
layout: default
title: Publications
---

# Publications

<div class="publications-list">
  {% for paper in site.data.papers %}
    <div class="paper-item" style="margin-bottom: 20px;">
      
      <div style="font-weight: bold; font-size: 1.1em;">
        <a href="{{ paper.url }}">{{ paper.title }}</a>
      </div>

      <div style="color: #444;">
        {{ paper.authors }}
      </div>

      <div style="font-style: italic; color: #666;">
        {{ paper.venue }} ({{ paper.year }})
      </div>

    </div>
  {% endfor %}
</div>