---
layout: page
title: Gallery
nav: true
nav_order: 7
permalink: /#gallery
---

<style>
  .carousel-img-container {
    width: 70%; /* 核心：强制占据父容器 70% 宽度 */
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .carousel-img-container img {
    width: 100%;    /* 图片填满 70% 的容器 */
    height: auto;   /* 保持长宽比 */
    object-fit: contain;
    border-radius: 8px; /* 可选：圆角看起来更现代 */
    box-shadow: 0 4px 10px rgba(0,0,0,0.1); /* 可选：增加阴影提升质感 */
  }

  /* 手机端适配：如果 70% 在手机上太小，可以恢复到 90% */
  @media (max-width: 768px) {
    .carousel-img-container {
      width: 90%;
    }
  }
</style>

<div id="galleryCarousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-wrap="true">
  <div class="carousel-inner">
    {% for photo in site.data.gallery %}
      <div class="carousel-item {% if forloop.first %}active{% endif %}">
        <div class="d-flex justify-content-center align-items-center" style="min-height: 400px; padding: 2rem 0;">
          <div class="carousel-img-container">
            <img src="{{ photo.image | prepend: 'assets/img/' | relative_url }}" alt="{{ photo.caption }}">
            {% if photo.caption %}
              <p style="margin-top: 1.5rem; font-size: 1.1rem; color: var(--global-text-color); text-align: center;">
                {{ photo.caption }}
              </p>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  
  <a class="carousel-control-prev" href="#galleryCarousel" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true" style="filter: invert(50%);"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#galleryCarousel" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true" style="filter: invert(50%);"></span>
    <span class="sr-only">Next</span>
  </a>
</div>