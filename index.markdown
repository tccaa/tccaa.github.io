---
layout: splash
title:
lang: en
permalink: /
header:
  overlay_color: "#000" # Overlay color in hex format
  overlay_filter: "0" # Opacity value from 0 to 1
  overlay_image: /assets/images/header.png # Path to your image
---

### Pinned Posts 置顶公告
<a href="/event/2025/01/08/2025_NewYear" target="_blank">
  <img src="/assets/images/events/2025_Spring_Flyer.001.png" alt="Centered Image" style="display: block; margin: 0 auto;" width="800">
</a>

### Recent Posts 近期动态
{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% include documents-collection.html entries=posts type=entries_layout %}
</div>

{% include paginator.html %}

### Event Calendar 活动日程
<div style="display: flex; justify-content: center; align-items: center;">
    <iframe src="https://calendar.google.com/calendar/embed?height=400&wkst=1&ctz=America%2FLos_Angeles&showPrint=0&mode=AGENDA&src=dGNjYWFuZXRAZ21haWwuY29t&color=%234285F4" style="border:solid 1px #777" width="400" height="400" frameborder="0" scrolling="no"></iframe>
</div>
