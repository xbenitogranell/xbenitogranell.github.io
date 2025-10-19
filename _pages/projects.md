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

*Thank you for visiting this site. Please bear with me as I update some projects's content*

This page summarizes some current research projects I'm leading, co-coordinating and participating, and are categorized into:

### **Paleoecological perspective of resilience**
I’m interested in studying critical transitions and non-linear ecosystem responses that are rarely captured in monitoring data, among other reasons, because environmental responses tend to be slow and lagged. I ask: What insights do abrupt transitions in the palaeoenvironmental record provide about the critical stressors and ecosystem response that give rise to the current state of socio-ecological systems? 

📗 I'm currently developing some of these ideas in two research projects ([DECISION](1_project) and [DELTAPULSE](9_project) focusing in the Ebro Delta and the potential for past environmental changes to induce long-lasting effects in ecosystem development (both natural and semi-natural habitats yet socio-environmentally relevant such as riche fields).

📗 The [PalaeOpen](4_project) COST Action aims at mobilizing multi-proxy paleoecological data communities, improve data sharing workflows (OPEN, FAIR), and inform current and future nature conservation projects. My involvement with **PalaeOpen** is on co-leading the aquatic proxies working group to find practical ways bridging aquatic communities (diatoms, chironomids, ostracods, testate amoeba, foraminifera) among them and with terrestrial ecosystems dynamics.


### **Long-Term Human-Environment dynamics**
There exists an increasing understanding that environmental issues are also social issues, and that past environmental changes cannot be fully understood if the human component is not accounted for because of the long-term occupied Earth ecosystems by humans since the last 20,000 years that influenced terrestrial and aquatic ecosystems, but also responded and adapted to environmental and climatic changes. I seek to foster interdisciplinary collaborations among paleolimnologists, paleoclimatologists, archaeologists, and other relevant disciplines to increase our predictive capacity of current and future climate change impacts on co-constructed human ecological niches.


📘 [Human Traces](8_project) is a [Past Global Changes](https://pastglobalchanges.org/science/wg/human-traces/intro) working group aiming at investigating the long-legacy of pre-Anthropocene human impacts in the sedimentary record synthesizing direct and indirect human evidences in the form of multidisciplinary databases.


📘 While the theoretical basis for fruitful interdisciplinary studies in paleosciences has already been identified, less efforts have been made in finding feasible strategies to put them into practice using inclusive and democratic approaches. The [pSESYNTH](5_project) project is a multi-year community mobilization grant to establish and strengthen regional, interdisciplinary teams for the study of Global South past socio-environmental systems across the Holocene.


### **Time series and global change impacts on aquatic ecosystems**
Freshwaters make disproportionate constributions to biochemical cycles and biodiversity, while coastal wetlands and deltas provide more ecosystem services than any other terrestrial biome for the same unit area. The densification of both freshwater and coastal water bodies (lentic and lotic systems) across the landscape has been used variously in limnology to understand (a)synchoronous responses to shared environmental and climatic forces, but there is no an unified framework based on the ecological and geographical drivers beyond monitoring observations. I’m interested in bridging the gap between physical geography and (paleo)limnology by investigating local and regional community dynamics (space) potentially connected by dispersal and changing through time, and the interactions between the two. 


📙 IRTA's Marine and Continental Waters Program is based in the Ebro Delta, one of the largest and ecologically significant coastal wetland in the Mediterranean. At the same time, it is impacted by hydrological alterations at the basin and delta scales, pollution, species invasions, and sea-level rise. We have different research contracts with the [Ebro Delta Natural Park](6_project) to examine the potential of biodiversity of time series (water quality, biological indicators, birds) to understand estuarine dynamics in the coastal lagoons, including, but not limited to: diatom diversity-productivity relationships, phytoplankton-macrophyte dominance states, ecological status, and conservation prioritization. 


📙 Most of the datasets characterizing water quality and ecological responses (biomass) are ecosystem-level specific (freshwater lentic/lotic, estuarine/coastal) and insufficiently unified and organized by connected hydro-systems. This precludes knowing if oligotrophication trends are coupled with biological responses or if it propagates into coastal areas. The main objective of [OLIGOTREND](3_project) is identify the ways in which nutrient oligotrophication trends across the aquatic continuum (rivers, streams, lakes, and estuaries) influence ecological dynamics, how these trends changed over time, and the possible synchrony of abrupt changes in phytoplankton vs macrophyted dominated states.


### **Diatom ecology and biogeography**
I study diatoms at different levels of biological organization to investigate long-term ecosystem variability and biogeographic patterns. At species level, I’m interested in how local and regional environmental factors dictate single-species distributions. At community level, I study assembly mechanisms (niche- and dispersal-based processes) to anticipate aquatic habitat changes.

📕 There exists an intrinsic disconnection between diatom researchers working on Iberoamerican aquatic ecosystems, whose research has been carried out mostly independently, often using different methodologies and diatom taxonomies as well as a systematic lack of data sharing protocols of FAIR and OPEN science. To enable the full potential for ecological and paleolimnological studies based on diatoms, the [SEED](2_project) project aims to mobilize communities and datasets to create the first Iberoamerican diatom database. 

📕 The collaborative network [IberRios](7_project) aims at collecting information on a wide range of river organisms (i.e. prokaryotes, fungi, algae, macrophytes, macroinvertebrates, fishes, amphibians, reptiles, birds and mammals) and ecosystem functions (e.g. carbon and nutrient cycling, pathogen control, thermal regulation) over multiple years (LTER) and across a large spatial scale, covering eight major river basins in the Iberian Peninsula.

### **Raising awareness about gender gaps in academia**
The Gender & Science group of the [Iberian Association of Limnology](https://limnetica.com/es/génerociencia) was created in 2014 to act as a gender observatory within the association and beyond, promote the role of women within the scientific community, and encourage gender equality measures in institutions directly or indirectly related to limnology.

<br><br>

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
