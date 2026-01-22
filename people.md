---
layout: default
title: People
---

# Team

{% assign groups = "PI,Postdoc,PhD,Alumni" | split: "," %}

{% for group in groups %}
  {% assign members = site.data.people | where: "group", group %}
  {% if members.size > 0 %}
    <h2 style="border-bottom: 2px solid #eee; padding-bottom: 10px;">{{ group }}</h2>
    <div class="people-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 20px; margin-bottom: 40px;">
      {% for person in members %}
        <div class="person-card">
          <img src="{{ person.image | relative_url }}" style="width: 100px; height: 100px; object-fit: cover; border-radius: 50%;">
          <h3><a href="{{ person.website }}">{{ person.name }}</a></h3>
          <p class="role">{{ person.role }}</p>
          <p class="bio" style="font-size: 0.9em; color: #666;">{{ person.bio }}</p>
        </div>
      {% endfor %}
    </div>
  {% endif %}
{% endfor %}