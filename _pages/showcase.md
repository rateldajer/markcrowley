---
layout: page
permalink: /showcase/
title: showcase
description: A selection of highlighted papers per year
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2009, 2007]
nav: false
showtitle: true
---

Also see:
- **[All Published Works](/publications)**
- [Publications Grouped by Research Topics](/pub-by-topic/)
- [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<h2>selected publications</h2>
<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers --max 10 -q @*[keywords~=showcase && year={{y}}, status^=1, self=1]* %}
{% endfor %}
</div> 
