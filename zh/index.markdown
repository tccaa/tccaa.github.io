---
layout: splash
title:
lang: zh
permalink: /zh/
header:
  overlay_color: "#000" # Overlay color in hex format
  overlay_filter: "0" # Opacity value from 0 to 1
  overlay_image: /assets/images/header.png # Path to your image
---
### 置顶消息

<img src="/assets/images/events/2025_SF_zh.JPG" alt="Centered Image" style="display: block; margin: 0 auto;" width="400">

<h2 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "近期动态" }}</h2>

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


