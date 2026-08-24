---
title: "Ice Fracture"
rank: 10
header:
  overlay_image: /assets/images/banner-fracture.jpg
  teaser: /assets/images/banner-fracture.jpg
  overlay_filter: 0.08
excerpt: <br><br><br><br><br><br><br><br><br>
---

## Papers 
<br>

<div class="entries-grid">
  {% assign sorted_pubs = site.publications | where_exp: "item", "item.categories contains 'fracture'" | sort: 'date' | reverse %}
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
