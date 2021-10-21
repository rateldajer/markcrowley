---
layout: page
permalink: /preprints/
title: preprints
description: Preprints and Working Papers
years: [2021, 2020, 2019]
nav: false
showtitle: true
---

Also see:
- [All Published Works](/publications)
- [Most Cited Publications](/mostcited)
- [Selected Showcase Publications](/showcase)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)

<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>
