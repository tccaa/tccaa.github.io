---
layout: splash
title:
lang: en
permalink: /
overlay_color: "#000" # Overlay color in hex format
  overlay_filter: "0" # Opacity value from 0 to 1
  overlay_image: /assets/images/header.png # Path to your image
---

<h3 style="text-align: center;">
  Pinned Posts 置顶公告 </h3>

  <a href="https://www.tccaa.org/event/2025/04/01/Mothers_Day/" target="_blank">
    <img src="https://www.tccaa.org/assets/images/events/2025_Mothers_Day_Flyer.png" alt="Centered Image" style="display: block; margin: 0 auto;" width="500">
  </a>

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
