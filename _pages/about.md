---
layout: about
title: About
permalink: /
subtitle: 林鹿宁

profile:
  align: right
  image: luninglin_pic.jpg
  image_circular: false
  more_info:
selected_papers: true
social: true

announcements:
  enabled: true
  scrollable: false
  limit: 100

latest_posts:
  enabled: false
---

I am currently a Ph.D. candidate specializing in Electronic Science and Technology at [Zhejiang University](https://www.zju.edu.cn/english/) (expected June 2026), where I am advised by [Prof. Zhiguo Shi](https://person.zju.edu.cn/shizg) (IEEE Fellow). I conduct my research within the [NESC Group](http://nesc.zju.edu.cn/) at the State Key Laboratory of Industrial Control Technology.
From September 2024 to September 2025, I was privileged to be a visiting scholar at the [University of Pisa](https://www.unipi.it/index.php/english), Italy, co-advised by [Prof. Fulvio Gini](https://scholar.google.com/citations?user=eKbNewIAAAAJ) (IEEE Fellow) and [Prof. Maria Sabrina Greco](https://scholar.google.com/citations?user=bZXCsFMAAAAJ) (IEEE Fellow).

My research is dedicated to the Integrated Sensing and Communication (ISAC), array signal processing, and wireless communication.
My findings have been featured in premier venues such as IEEE TSP, IEEE TAES, and IEEE SPL, and presented at flagship conferences including ICASSP and RadarConf.
Beyond my research, I actively contribute to the academic community as an independent reviewer for journals like IEEE TSP, TAES, TMTT, SPL, and TVT, as well as confereces including IEEE ICASSP, RadarConf, Globecom, ICC, PIMRC, VTC, etc.

Outside of the lab, I am a passionate long-distance runner and love melodies. Feel free to reach out if you'd like to chat about tech, running, or anything in between! ✨

<!-- Photo Gallery -->
{% if site.data.gallery %}
  <h2 id="gallery">📷 Gallery</h2>
  <div class="photo-gallery">
    <div id="galleryCarousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-wrap="true">
      <div class="carousel-inner">
        {% for photo in site.data.gallery %}
          <div class="carousel-item {% if forloop.first %}active{% endif %}">
            <div class="d-flex justify-content-center align-items-center" style="padding: 1rem;">
              <div style="text-align: center; max-width: 70%; margin: 0 auto;">
                <img src="{{ photo.image | prepend: 'assets/img/' | relative_url }}" alt="{{ photo.caption }}" style="max-width: 100%; height: auto; display: inline-block;">
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
  </div>
  
  <hr style="border-top: 2px solid var(--global-divider-color); margin: 2rem 0;">
{% endif %}
