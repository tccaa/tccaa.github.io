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

<h3 style="text-align: center;">
  Pinned Posts 置顶公告 </h3>

  <a href="https://photos.app.goo.gl/dLEwmXaRKzRgC78K8" target="_blank">
    <img src="https://lh3.googleusercontent.com/pw/AP1GczMLFu6xvHuNo82VNv1OdFV3wJiEY2LrL1bzFjDsojBRgx94Hh36jXHJ5pHXCRUEchhhf2Kdy727OZJ9OzgWIfU6cCBvu85lMvX6xS-2rY-KBgLFKYyZ38c6hfjLPARHkzPOSNcZOlY9iCd7DF-8UvxS9A=w1898-h1266-s-no-gm?authuser=0" alt="Centered Image" style="display: block; margin: 0 auto;" width="800">
  </a>

<h2 style="text-align: center;">
  2025 Lunar New Year Gala <a href="https://photos.app.goo.gl/dLEwmXaRKzRgC78K8">Photos</a> and <a href="https://youtu.be/zbVs_Sa7SBA?si=71FWizcov61Ktm5i">Video</a> are Online
</h2>

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
