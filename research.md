---
layout: splash # archive
title: "Research"
permalink: /research/
author_profile: false
header:
  overlay_image: /assets/images/banner-research.jpg
  overlay_filter: 0.1
excerpt: "<br><br><br><br><br>"
---

{% assign topics = site.research | sort: "rank" %}

<div class="entries-grid">
  {% for topic in topics %}
   <div class="grid__item">
      <div class="research-item__thumbnail">
        <a href="{{ topic.url | relative_url }}">
          <img src="{{ topic.header.teaser | relative_url }}" alt="{{ topic.title }}">
        </a>
      </div>
      <div class="research-item__content">
      <center>
        <h4 class="research-item__title">
          <a href="{{ topic.url | relative_url }}">{{ topic.title }}</a>
        </h4>
        </center>
      </div>
    </div>
  {% endfor %}
</div>
