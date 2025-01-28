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

<!-- Carousel -->
<div class="carousel-container">
  <div id="carouselExample" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="/assets/images/events/2025_SF_zh.JPG" class="d-block w-100" alt="Slide 1">
      </div>
      <div class="carousel-item">
        <img src="https://lh3.googleusercontent.com/pw/AP1GczNB-ibXPlOE0AcrKJzT1VumyuH5Fo7Nq-8jxj-akmCj2ALxjL8GXjk62JraXe9wopL3AXW57S2SE7AJkQZhOb3njjzd4IFtEtk3eSOfPb-Ru2YxPn9jq0Y-fvl4SXs0n1XdG_g2W3eLlPymtItFFgmNMw=w2264-h1698-s-no-gm?authuser=0" class="d-block w-100" alt="Slide 2">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</div>

### Event Calendar 活动日程
<div style="display: flex; justify-content: center; align-items: center;">
    <iframe src="https://calendar.google.com/calendar/embed?height=400&wkst=1&ctz=America%2FLos_Angeles&showPrint=0&mode=AGENDA&src=dGNjYWFuZXRAZ21haWwuY29t&color=%234285F4" style="border:solid 1px #777" width="400" height="400" frameborder="0" scrolling="no"></iframe>
</div>

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