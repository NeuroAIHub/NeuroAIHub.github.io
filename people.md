---
layout: default
title: People
---

# Team

<div>
{% assign groups = "PI,Postdoc,PhD,Alumni" | split: "," %}

{% for group in groups %}
{% assign members = site.data.people | where: "group", group %}
{% if members.size > 0 %}

<h2 style="border-bottom: 2px solid #eee; padding-bottom: 10px; margin-top: 30px;">{{ group }}</h2>

<div class="people-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 20px; margin-bottom: 40px;">
{% for person in members %}
<div class="person-card">
{% if person.image %}
<img src="{{ person.image | relative_url }}" style="width: 100px; height: 100px; object-fit: cover; border-radius: 50%; display: block; margin-bottom: 10px;">
{% endif %}
<h3 style="margin: 5px 0;"><a href="{{ person.website }}" style="text-decoration: none; color: #333;">{{ person.name }}</a></h3>
<p class="role" style="font-weight: bold; color: #555; margin: 5px 0;">{{ person.role }}</p>
<p class="bio" style="font-size: 0.9em; color: #666; margin: 0;">{{ person.bio }}</p>
</div>
{% endfor %}
</div>

{% endif %}
{% endfor %}
</div>