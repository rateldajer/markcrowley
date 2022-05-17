---
layout: page
permalink: /publications/
title: publications
description: Published papers from my lab.
years: [2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2014, 2013, 2012, 2011, 2010, 2009,2007, 2005]
nav: true
showtitle: true
---

Also see:
- [Selected Showcase Publications](/showcase)
- [Publications Grouped by Research Topics](/pub-by-topic/)
- [Current Preprints and Working Papers](/preprints) / [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}},status^=1,self=1]* %}
{% endfor %}
</div>
