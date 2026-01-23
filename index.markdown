---
layout: splash
title:
lang: en
permalink: /
header:
  overlay_color: "transparent" # Overlay color in hex format
  overlay_filter: "0" # Opacity value from 0 to 1
  overlay_image: /assets/images/header_tighter.PNG # Path to your image
---

<h3 style="text-align: center;">
  Pinned Posts 置顶公告 </h3>

  <div style="text-align: center;">
  <img src="/assets/images/events/2026/2026_NewYear_En.jpg" alt="2026 Lunar New Year English Poster" style="display: inline-block; margin: 10px; width: 400px; height: auto; max-width: 45%;">
  <img src="/assets/images/events/2026/2026_NewYear_Zh.jpg" alt="2026 Lunar New Year Chinese Poster" style="display: inline-block; margin: 10px; width: 400px; height: auto; max-width: 45%;">
  </div>

<h3 style="text-align: center;">
  Recent Posts 近期动态 </h3>

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

<h3 style="text-align: center;">
  Event Calendar 活动日程 </h3>

<div style="display: flex; justify-content: center; align-items: center;">
    <iframe src="https://calendar.google.com/calendar/embed?height=400&wkst=1&ctz=America%2FLos_Angeles&showPrint=0&mode=AGENDA&src=dGNjYWFuZXRAZ21haWwuY29t&color=%234285F4" style="border:solid 1px #777" width="400" height="400" frameborder="0" scrolling="no"></iframe>
</div>
