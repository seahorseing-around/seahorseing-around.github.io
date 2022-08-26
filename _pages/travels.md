---
layout: page
title: travels
permalink: /travels/
description: A place for me to remember my adventures.
nav: true
nav_order: 5
display_categories: [fun, travel]
horizontal: false
---

<!-- pages/travels.md -->
<div class="travels">
{%- if site.enable_travel_categories and page.display_categories %}
  <!-- Display categorized travels -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_travels = site.travels | where: "category", category -%}
  {%- assign sorted_travels = categorized_travels | sort: "importance" %}
  <!-- Generate cards for each travel -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for travel in sorted_travels -%}
      {% include travels_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for travel in sorted_travels -%}
      {% include travels.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display travels without categories -->
  {%- assign sorted_travels = site.travels | sort: "importance" -%}
  <!-- Generate cards for each travel -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for travel in sorted_travels -%}
      {% include travels_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for travel in sorted_travels -%}
      {% include travels.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
