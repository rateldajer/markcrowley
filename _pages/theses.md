---
layout: page
permalink: /theses/
title: student theses
titleheader: student theses
description: A selection of completed graduate theses from the lab by year
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018]
nav: false
showtitle: true
shownotes: true
showcitations: true
---

Also see:
- **[All Published Works](/publications)**
- **[Selected Showcase Publications](/showcase)**
- [Publications Grouped by Research Topics](/pub-by-topic/)
- [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<!-- <h2>selected publications</h2> -->
<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f theses --max 10 -q @*[type~=thesis && year={{y}}, status^=1]* %}
{% endfor %}
</div> 
