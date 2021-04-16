---
layout: page
permalink: /publications/
title: publications
description: Recent published work out of the lab.
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015]
nav: true
showtitle: true
---

<div class="publications by year">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
