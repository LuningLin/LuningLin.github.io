---
layout: page
title: Gallery
nav: true
nav_order: 7
permalink: /gallery/
---

<style>
  /* 强制轮播图区域撑满屏幕（可选） */
  .carousel-item {
    text-align: center;
  }

  .carousel-img-container {
    /* 核心修改：使用屏幕宽度的 70% */
    width: 70vw !important; 
    max-width: 1100px; /* 设置一个合理的上限 */
    margin: 0 auto;
  }

  .carousel-img-container img {
    width: 100% !important;
    height: auto !important;
    display: block;
    border-radius: 12px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
  }

  @media (max-width: 768px) {
    .carousel-img-container {
      width: 95vw !important; /* 手机端几乎全屏 */
    }
  }
</style>

<div id="galleryCarousel" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    {% for photo in site.data.gallery %}
      <div class="carousel-item {% if forloop.first %}active{% endif %}">
        <div class="d-flex justify-content-center py-5">
          <div class="carousel-img-container">
            <img src="{{ photo.image | prepend: 'assets/img/' | relative_url }}" alt="{{ photo.caption }}">
            {% if photo.caption %}
              <p class="mt-3" style="color: var(--global-text-color); opacity: 0.8;">{{ photo.caption }}</p>
            {% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  
  <a class="carousel-control-prev" href="#galleryCarousel" data-slide="prev" style="filter: invert(1);">
    <span class="carousel-control-prev-icon"></span>
  </a>
  <a class="carousel-control-next" href="#galleryCarousel" data-slide="next" style="filter: invert(1);">
    <span class="carousel-control-next-icon"></span>
  </a>
</div>