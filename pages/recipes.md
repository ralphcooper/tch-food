---
layout: splash
title: All Recipes
permalink: "/recipes/"
excerpt: "A big old list of the recipes we know"
header:
  overlay_image: /assets/images/evening-dinner.jpg
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
classes: wide
---
<style>
  .grid-container {
    display: grid;
    grid-template-columns: auto auto auto auto;
    grid-gap: 10px;
    padding: 10px;
  }

  .grid-container > div {
    text-align: center;
    padding: 10px 0;
    
  }
</style>

<div class="grid-container" style="grid-auto-flow: row;">
  {% for recipe in site.recipes %}
    <div>
      <a href="{{ recipe.url }}">
        {% if recipe.header.overlay_image %}
          <img src="{{recipe.header.overlay_image}}" width=180 height=180 />
        {% else %}
          <img src="http://placehold.it/180" width=180 height=180 />
        {% endif %}
        <br />
        <b>{{ recipe.title }}</b>
      </a>
      <br/>
      <span>{{ recipe.blurb | markdownify }}</span>
    </div>
  {% endfor %}
</div>


