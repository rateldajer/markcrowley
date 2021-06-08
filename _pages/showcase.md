---
layout: page
permalink: /showcase/
title: showcase
description: Showcase of Highlighted Papers
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011]
nav: false
showtitle: true
---

Also see:
- [All Published Works](/publications)
- [Current Preprints and Working Papers](/preprints)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<h2>selected publications</h2>
<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers --max 50 -q @*[keywords~=showcase && year={{y}}]* %}
{% endfor %}
</div> 
