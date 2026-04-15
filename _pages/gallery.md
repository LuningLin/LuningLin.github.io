---
layout: page
title: Gallery
nav: true
nav_order: 2
permalink: /gallery/
---

<div id="galleryCarousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-wrap="true" style="max-width: 70%; margin: 0 auto;">
  <div class="carousel-inner">
    {% for photo in site.data.gallery %}
      <div class="carousel-item {% if forloop.first %}active{% endif %}">
        <div class="d-flex justify-content-center align-items-center" style="padding: 2rem;">
          <div style="text-align: center;">
            <img class="d-block w-100" src="{{ photo.image | prepend: 'assets/img/' | relative_url }}" alt="{{ photo.caption }}" style="height: auto; object-fit: contain;">
            {% if photo.caption %}
              <p style="margin-top: 1rem; font-size: 1rem; color: var(--global-text-color);">{{ photo.caption }}</p>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  <a class="carousel-control-prev" href="#galleryCarousel" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#galleryCarousel" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>