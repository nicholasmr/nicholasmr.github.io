---
layout: splash
title: "People"
permalink: /people/
author_profile: false
header:
  overlay_image: /assets/images/banner-people.jpg
  overlay_filter: 0.20
excerpt: <br><br><br><br>
---

{% assign currentgroup = site.people | where: "current", "yes" | sort: "category" | sort: "rank" %}

# Current Group Members

Our group is a collaborative environment of faculty, postdocs, and students (PhD, Master's, and Undergraduate) focused on the physics of ice flow and glaciological modeling. Our work integrates field data (ice cores, geophysical surveys) with models of large-scale ice sheet dynamics, small-scale deformation physics, and time-evolving boundary conditions. 
<br><br> 

<div class="entries-grid">
  {% for person in currentgroup %} 
<div class="grid__item">
      <div class="team-member__avatar">
        <img src="{{ person.avatar | relative_url }}" alt="{{ person.title }}">
      </div>
      <div class="team-member__content">
        <h4 class="team-member__name">{{ person.title }}</h4>
        <p class="team-member__position">{{ person.position }}</p>
        <p class="team-member__bio">{{ person.excerpt }}</p>
      </div>
</div>
  {% endfor %}
</div>




