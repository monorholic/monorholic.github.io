---
layout: single
author_profile: true
permalink: /
header:
  overlay_color: "#ffffff"
  overlay_filter: linear-gradient(rgba(95, 75, 139, 0.8),rgba(0, 171, 192, 0.8))
---

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>

{% include paginator.html %}
