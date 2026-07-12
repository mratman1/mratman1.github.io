---
title: "Cats"
permalink: /cats/
layout: single
author_profile: true
---

## Pictures of my Cats

{% assign photo_count = 0 %}
{% for file in site.static_files %}
  {% if file.path contains "/assets/images/cats/" %}
    {% case file.extname %}
      {% when ".jpg" or ".jpeg" or ".png" or ".gif" or ".webp" %}
        {% assign photo_count = photo_count | plus: 1 %}
    {% endcase %}
  {% endif %}
{% endfor %}

{% if photo_count > 0 %}
<div class="cat-gallery">
  {% for file in site.static_files %}
    {% if file.path contains "/assets/images/cats/" %}
      {% case file.extname %}
        {% when ".jpg" or ".jpeg" or ".png" or ".gif" or ".webp" %}
  <a href="{{ file.path | relative_url }}" target="_blank" rel="noopener" class="cat-gallery__item">
    <img src="{{ file.path | relative_url }}" alt="Cat photo" loading="lazy">
  </a>
      {% endcase %}
    {% endif %}
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
