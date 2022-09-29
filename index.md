---
author: vietzettt
layout: home
title: "🎉no_r3m0rs3@mpei.ru🎉"
permalink: /
---
{%- for post in site.posts -%}
  {%- capture current_year -%}{{ post.date | date: "%Y" }}{%- endcapture -%}
  {%- unless current_year == previous_year -%}
    <h3 align="center">{{ current_year }}</h3>
    {%- assign previous_year = current_year -%}
  {%- endunless -%}
  <article class="post-item" align="center">
    <h6 class="post-item-title">
      <a href="{{ post.url }}">{{ post.title | escape }}</a>
    </h6>
  </article>
{%- endfor -%}