---
layout: default
permalink: /catalog/

pre: Titch
title: Catalog
---
<section class="catalog">
{% for item in site.catalog %}
  <a href="{{ item.url }}">
    <figure>
      <img src="/i{{ item.url }}/01_360w.jpg" alt="{{ item.title }}">
      <figcaption>
        {{ item.title }}
      </figcaption>
    </figure>
  </a>
{% endfor %}
</section>