---
title: "Maths"
permalink: /maths/
layout: single
author_profile: true
---

{% assign math_posts = site.categories.maths | sort: 'date' | reverse %}
{% if math_posts.size > 0 %}
<ul class="math-post-list">
  {% for post in math_posts %}
  <li class="math-post-list__item">
    <a class="math-post-list__title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="math-post-list__date">{{ post.date | date: "%B %-d, %Y" }}</span>
  </li>
  {% endfor %}
</ul>
{% else %}
*No posts yet — add a file to `_posts/` with `categories: maths` and it'll show up here automatically.*
{% endif %}
