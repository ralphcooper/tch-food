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
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));;
    grid-gap: 0.5rem;
    padding: 10px;
    justify-items: center;
  }

  .grid-item {
    padding: 1rem;
    justify-self: center;
  }

  .square {
    width: 180px;
    height: 180px;
    overflow: hidden;
  }

  .wrap {
    min-width: 0;
    min-height: 0;
    word-break: break-word;
    max-width: 100%;
    text-align: center;
  }
</style>

<div class="grid-container" style="grid-auto-flow: row;">
  {% for recipe in site.recipes %}
    <div class="grid-item">
      <a href="{{ recipe.url }}">
        <div class="square">
        {% if recipe.header.overlay_image %}
          <img src="{{recipe.header.overlay_image}}" width=180 height=180 />
        {% else %}
          <img src="http://placehold.it/180" width=180 height=180 />
        {% endif %}
        </div>
        <p class="wrap">
          <b>{{ recipe.title }}</b>
        </p>
      </a>
    </div>
  {% endfor %}
</div>


