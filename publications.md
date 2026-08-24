---
layout: splash # archive
title: "Publications"
permalink: /publications/
author_profile: false
header:
  overlay_image: /assets/images/banner-welcome.jpg
  overlay_filter: 0.1
excerpt: "<br><br><br><br><br>"
---

<div class="entries-grid">
  {% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
  {% for paper in sorted_pubs %}
    <div class="grid__item">
      <div class="research-item__thumbnail">
        <a href="{{ paper.paperurl }}" target="_blank" rel="noopener noreferrer">
          <img src="{{ paper.header.teaser | relative_url }}" alt="{{ paper.title }}">
        </a>
      </div>
      <div class="research-item__content">
          <div style="margin: 19px 0 0 0; font-size: 1rem;"> <b>{{ paper.authors }} ({{ paper.date | date: "%Y" }})</b> </div>
          <div style="margin: 6px 0 0 0; font-size: 0.95rem;"> <i>{{ paper.title }}</i> </div>
      </div>
    </div>
  {% endfor %}
</div>
