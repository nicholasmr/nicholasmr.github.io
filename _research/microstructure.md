---
title: "Ice Microstructure"
rank: 5
header:
  teaser: /assets/images/banner-microstructure.jpg
  overlay_color: "#000"
excerpt: >
    <video autoplay loop muted playsinline class="hero-video"><source src="/assets/images/banner-microstructure.mp4" type="video/mp4"></video>
    <br><br><br><br><br><br><br><br><br>
---

## Papers 

<div class="entries-grid">
  {% assign sorted_pubs = site.publications | where_exp: "item", "item.categories contains 'microstructure'" | sort: 'date' | reverse %}
  {% for paper in sorted_pubs %}
    <div class="grid__item">
      <div class="research-item__thumbnail">
        <a href="{{ paper.paperurl }}" target="_blank" rel="noopener noreferrer">
          <img src="{{ paper.header.teaser | relative_url }}" alt="{{ paper.title }}">
        </a>
      </div>
      <div class="research-item__content">
          <div style="margin: 15px 0 0 0; font-size: 0.9rem;"> <i>{{ paper.title }}</i> </div>
          <div style="margin: 7px 0 0 0; font-size: 0.9rem;"> <b>{{ paper.authors }}</b> </div>
          <small><i>{{ paper.venue }}</i>, {{ paper.date | date: "%Y" }}</small>
      </div>
    </div>
  {% endfor %}
</div>
