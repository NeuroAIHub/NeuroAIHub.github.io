---
layout: default
title: Publications
---

# Publications

<div class="bibliography">
{% bibliography %}
  <div class="paper-entry" style="display: flex; margin-bottom: 40px; gap: 20px;">
    <div class="paper-preview" style="flex: 0 0 200px;">
      {% if entry.preview %}
        <img src="{{ entry.preview | relative_url }}" style="width: 100%; border-radius: 4px; border: 1px solid #eee;">
      {% endif %}
    </div>

    <div class="paper-details">
      <div class="title" style="font-weight: bold; font-size: 1.1em;">
        <a href="{{ entry.url }}">{{ entry.title }}</a>
      </div>
      <div class="authors" style="color: #555; margin: 5px 0;">
        {{ entry.author_string }}
      </div>
      <div class="venue" style="font-style: italic; color: #777;">
        {{ entry.journal }}{{ entry.booktitle }} ({{ entry.year }})
      </div>
      
      {% if entry.tldr %}
      <div class="tldr" style="background: #f5f5f5; padding: 8px; border-radius: 4px; margin-top: 8px; font-size: 0.9em;">
        <strong>TL;DR:</strong> {{ entry.tldr }}
      </div>
      {% endif %}
    </div>
  </div>
{% endbibliography %}
</div>