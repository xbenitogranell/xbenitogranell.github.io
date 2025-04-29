---
layout: page
title: research
permalink: /projects/
description: 
nav: true
nav_order: 1
display_categories: false
horizontal: false
---

*Thank for you visiting this site. Please bear with me as I update some projects's content*
This page summarizes some current research projects I'm leading, co-coordinating and participating, and are categorized into:

1.**Paleoecological perspective of resilience**
I’m interested in studying critical transitions and non-linear ecosystem responses that are rarely captured in monitoring data, among other reasons, because environmental responses tend to be slow and lagged. I ask: What insights do abrupt transitions in the palaeoenvironmental record provide about the critical stressors and ecosystem response that give rise to the current state of socio-ecological systems? 

I'm currently developing some of these ideas in the research project [DECISION](1_project) focusing in the Ebro Delta and the potential for past environmental changes to induce long-lasting effects in ecosystem development (both natural and semi-natural habitats).


2.**Spatio-temporal community dynamics**
The densification of water bodies (lentic and lotic systems) across the landscape has been used variously in limnology, but there is no an unified framework based on the ecological and geographical drivers beyond monitoring observations. I’m interested in bridging the gap between physical geography and limnology by investigating local and regional community dynamics (space) potentially connected by dispersal and changing through time, and the interactions between the two.


3.**Time series and global change impacts on aquatic ecosystems**
Freshwaters make disproportionate constributions to biochemical cycles and biodiversity, while coastal wetlands and deltas provide more ecosystem services than any other terrestrial biome for the same unit area. Employing a multidisciplinary approach, I combine traditional ecological and palaeoecological approaches to study past, present and future Mediterranean coastal wetland ecosystems and tropical freshwaters.


4.**Diatom ecology and biogeography**
I study diatoms at different levels of biological organization to investigate long-term ecosystem variability and biogeographic patterns. At species level, I’m interested in how local and regional environmental factors dictate single-species distributions. At community level, I study assembly mechanisms (niche- and dispersal-based processes) to anticipate ecosystem response to environmental changes.


5.**Raising awareness about gender gaps in academia**


<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
