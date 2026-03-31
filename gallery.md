---
layout: page
title: Photo Gallery
subtitle: Outreach in Action!
comments: false
---


Enjoy some photo galleries from our various events!  

<div class="gallery">
  {% for img in site.data.gallery_page %}
  <div class="gallery-item">
    <a href="#img{{ forloop.index }}">
      <img src="{{ img.file }}" alt="{{ img.alt }}">
      <div class="gallery-caption">{{ img.caption }}</div>
    </a>
  </div>
  {% endfor %}
</div>

<!-- --- Lightboxes --- -->
{% for img in site.data.gallery_page %}
<div id="img{{ forloop.index }}" class="lightbox">
  <div class="lightbox-image-wrapper">
    <a href="#!" class="close">×</a>
    <img src="{{ img.file }}" alt="{{ img.alt }}">
    <div class="lightbox-caption">{{ img.caption }}</div>
  </div>

  <a href="#img{% if forloop.first %}{{ site.data.gallery | size }}{% else %}{{ forloop.index0 }}{% endif %}" class="prev">&#10094;</a>
  <a href="#img{% if forloop.last %}1{% else %}{{ forloop.index | plus:1 }}{% endif %}" class="next">&#10095;</a>
</div>
{% endfor %}

<!-- --- Gallery Section --- 
<div class="gallery">
  <div class="gallery-item">
    <a href="#img1">
      <img src="/assets/img/wellframe.jpg" alt="Construction of mirror pit illusion frame.">
      <div class="gallery-caption">We made a bottomless pit!</div>
    </a>
  </div>
  <div class="gallery-item">
    <a href="#img2">
      <img src="/assets/img/scrimcloseup.jpg" alt="Light shining through a scrim.">
      <div class="gallery-caption">Here be dragons.</div>
    </a>
  </div>
  <div class="gallery-item">
    <a href="#img3">
      <img src="/assets/img/middle_1.jpg" alt="Family STEM night at a Rochester middle school.">
      <div class="gallery-caption">Go go middle schoolers!</div>
    </a>
  </div>
</div>

<!-- --- Lightboxes with Next/Prev --- 
<div id="img1" class="lightbox">
  <a href="#">×</a>
  <a href="#img3" class="prev">&#10094;</a>
  <img src="/assets/img/wellframe.jpg" alt="Construction of mirror pit illusion frame."> <!-- copy this line from above --
  <a href="#img2" class="next">&#10095;</a>
</div>

<div id="img2" class="lightbox">
  <a href="#">×</a>
  <a href="#img1" class="prev">&#10094;</a>
  <img src="/assets/img/scrimcloseup.jpg" alt="Light shining through a scrim."> <!-- copy this line from above --
  <a href="#img3" class="next">&#10095;</a>
</div>

<div id="img3" class="lightbox">
  <a href="#">×</a>
  <a href="#img2" class="prev">&#10094;</a>
  <img src="/assets/img/middle_1.jpg" alt="Go go middle schoolers!">
  <img src="/assets/img/middle_1.jpg" alt="Family STEM night at a Rochester middle school."><!-- copy this line from above --
  <a href="#img1" class="next">&#10095;</a>
</div>




<!--
wooapsd 
![word?](/assets/img/wellboards.jpg){: .mx-auto.d-block :}

wasdjfal tration:
![wrod!](/assets/img/wellframe.jpg){: .mx-auto.d-block :}
-->

