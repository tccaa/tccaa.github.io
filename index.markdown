---
layout: default
title:
lang: en
permalink: /
---
<div class="page__hero" style="background-image: url('/assets/images/header.png'); height: 200px; background-size: cover; background-position: center;">
</div>

### Pinned Posts 置顶公告

<img src="/assets/images/events/2025_SF_en.JPG" alt="Centered Image" style="display: block; margin: 0 auto;" width="400">

### Event Calendar 活动日程
<div style="display: flex; justify-content: center; align-items: center; min-height: 100vh;">
    <iframe src="https://calendar.google.com/calendar/embed?height=600&wkst=1&ctz=America%2FLos_Angeles&src=dGNjYWFuZXRAZ21haWwuY29t&color=%234285F4" style="border:solid 1px #777" width="500" height="400" frameborder="0" scrolling="no"></iframe>
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

