---
layout: splash
author_profile: false # Usually hidden on splash pages for a cleaner look
header:
  overlay_image: /assets/images/banner-welcome.jpg
  overlay_filter: 0.1 
excerpt: "at Physics of Ice Climate and Earth, Niels Bohr Institute<br>"
---

# About

We investigate the past and future evolution of the Greenland and Antarctic ice sheets to better understand Earth’s climate history and project future sea-level rise. Our research integrates large-scale ice sheet dynamics and small-scale deformation physics with time-evolving boundary conditions. To bridge theory and observation, we constrain our models using unique field data from ice cores and geophysics (radar, seismics) alongside high-resolution satellite datasets.

Our methodology is characterized by a bottom-up approach to building models while also relying on established large-scale ice flow and regional climate model softwares. Embedded within the ice-core and geophysics section, our work is very interdisciplinary, merging data products and methods from the broader Earth system and climate sciences. Our approach is anchored in active field programs in Greenland and Antarctica, where we conduct ice-core drilling and collect ice-penetrating radar data to resolve the internal structure and history of the ice.

<section class="splide" id="pub-carousel" aria-label="Recent Publications">
<div class="splide__track"  style="margin-left:0%; margin-right:0%;">
<ul class="splide__list">
{% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
{% for paper in sorted_pubs %}
<li class="splide__slide">
    <div class="grid__item">
      <div class="research-item__thumbnail">
        <a href="{{ paper.paperurl }}" target="_blank" rel="noopener noreferrer">
          <img src="{{ paper.header.teaser | relative_url }}" alt="{{ paper.title }}">
        </a>
      </div>
      <div class="research-item__content">
          <div style="margin: 25px 0 0 0; font-size: 0.9rem;"> <b>{{ paper.authors}} ({{ paper.date | date: "%Y" }})</b> </div>
          <div style="margin: 5px 0 0 0; font-size: 0.9rem;"> <i>{{ paper.title | truncate: 50 }}</i> </div>
      </div>
    </div>
</li>
{% endfor %}
</ul>
</div>
</section>

<script>
  document.addEventListener('DOMContentLoaded', function () {
    new Splide('#pub-carousel', {
      type   : 'loop',
      arrows : false,  // This hides the left/right arrows
      perPage: 3,      // Number of papers visible at once
      gap    : '0rem',
      autoplay: true,
      interval: 4000,
      breakpoints: {
        1024: { perPage: 2 }, // Tablets
        640 : { perPage: 1 }, // Mobile
      }
    }).mount();
  });
</script>

# Meeting calendar

<div class="calendar-container">
  <iframe src="https://calendar.google.com/calendar/embed?src=cicmodelling%40gmail.com&ctz=Europe/Brussels&mode=AGENDA" style="border: 0" width="1200" height="500" frameborder="0" scrolling="no"></iframe>
</div>


