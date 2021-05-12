---
layout: page
permalink: /publications/
title: publications
description: Recent published work out of the lab.
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2014, 2013, 2012, 2011, 2010, 2009]
nav: true
showtitle: true
---

Also see:
- [Selected Showcase Publications](/showcase)
- [Current Preprints and Working Papers](/preprints)

<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}},status^=1]* %}
{% endfor %}

</div>
