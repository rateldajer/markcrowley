---
layout: page
permalink: /showcase/
title: showcase
description: A selection of highlighted papers per year
years: [2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
nav: false
showtitle: true
---

Also see:
- [All Published Works](/publications)
- [Current Preprints and Working Papers](/preprints) / [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<h2>selected publications</h2>
<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers --max 50 -q @*[keywords~=showcase && year={{y}}]* %}
{% endfor %}
</div> 
