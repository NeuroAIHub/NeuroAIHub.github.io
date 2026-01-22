---
layout: default
title: Publications
---

# Publications

<div class="publications-list">
  {% for paper in site.data.papers %}
    <div class="paper-item" style="margin-bottom: 30px; padding-bottom: 30px; border-bottom: 1px solid #eee;">

      <div style="display: flex; gap: 20px; align-items: start;">
        {% if paper.img %}
        <div class="paper-image" style="flex-shrink: 0;">
          <img src="{{ paper.img | relative_url }}" alt="{{ paper.title }}" style="width: 150px; height: 150px; object-fit: cover; border-radius: 4px; border: 1px solid #ddd;">
        </div>
        {% endif %}

        <div class="paper-content" style="flex: 1;">
          <div style="font-weight: bold; font-size: 1.1em; margin-bottom: 8px;">
            <a href="{{ paper.url }}" style="text-decoration: none; color: #333;">{{ paper.title }}</a>
          </div>

          <div style="color: #444; margin-bottom: 5px;">
            {{ paper.authors }}
          </div>

          <div style="font-style: italic; color: #666; margin-bottom: 10px;">
            {{ paper.venue }} ({{ paper.year }})
          </div>

          {% if paper.tldr %}
          <div class="paper-tldr" style="background: #f8f9fa; padding: 10px 15px; border-left: 3px solid #007bff; border-radius: 3px; font-size: 0.95em; color: #555; line-height: 1.5;">
            <strong>TL;DR:</strong> {{ paper.tldr }}
          </div>
          {% endif %}
        </div>
      </div>

    </div>
  {% endfor %}
</div>

<style>
  @media (max-width: 768px) {
    .paper-item {
      flex-direction: column !important;
    }

    .paper-image img {
      width: 100% !important;
      max-width: 200px;
    }
  }
</style>