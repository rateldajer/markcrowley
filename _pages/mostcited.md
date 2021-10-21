---
layout: page
permalink: /mostcited/
title: most cited
description: Showcase of Highlighted Papers
citations: [80, 60, 40, 20, 10]
nav: false
showtitle: true
---

Also see:
- [All Published Works](/publications)
- [Selected Showcase Publications](/showcase)
- [Current Preprints and Working Papers](/preprints)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<h2>selected publications</h2>
<div class="publications by year">
{% for c in page.citations %}
  <h2 class="year">>={{c}}</h2>
  {% bibliography -f papers --max 50 -q @*[citations>={{c}}]* %}
{% endfor %}
</div> 
