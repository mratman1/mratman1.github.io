---
title: "Cats"
permalink: /cats/
layout: single
author_profile: true
---

## Pictures of my Cats

{% assign cat_photos = site.static_files | where_exp: "file", "file.path contains '/assets/images/cats/'" %}
{% assign cat_photos = cat_photos | where_exp: "file", "file.extname == '.jpg' or file.extname == '.jpeg' or file.extname == '.png' or file.extname == '.gif' or file.extname == '.webp'" %}

{% if cat_photos.size > 0 %}
<div class="cat-gallery">
  {% for photo in cat_photos %}
  <a href="{{ photo.path | relative_url }}" target="_blank" rel="noopener" class="cat-gallery__item">
    <img src="{{ photo.path | relative_url }}" alt="Cat photo" loading="lazy">
  </a>
  {% endfor %}
</div>

<style>
.cat-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 1em;
  margin: 1.5em 0;
}
.cat-gallery__item {
  display: block;
  overflow: hidden;
  border-radius: 0.5em;
}
.cat-gallery__item img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: block;
  transition: transform 0.2s ease;
}
.cat-gallery__item:hover img {
  transform: scale(1.05);
}
</style>
{% else %}
*No photos yet — drop image files into `assets/images/cats/` and they'll show up here automatically.*
{% endif %}
