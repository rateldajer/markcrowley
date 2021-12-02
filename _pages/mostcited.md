---
layout: page
permalink: /mostcited/
title: most cited
description: Showcase of Highlighted Papers
nav: false
showtitle: true
publish: false
---
`TODO: fixing bugs`


Also see:
- [All Published Works](/publications)
- [Selected Showcase Publications](/showcase)
- [Current Preprints and Working Papers](/preprints)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)


<h2>selected publications</h2>
<div class="publications by year">
{% for b in (1..100) reversed %}
  {% assign c = b | modulo: 20 %}
    {% if c == 0 %}
      {% assign low = b %}
      {% assign high = b | plus: 20 %}
      <h2 class="year">>={{b}}</h2>
      yes! {{low}}-{{high}}
      {% bibliography -f papers --max 5 -q @*[citations>={{low}} & citations<{{high}}]* %}
    {% endif %}
{% endfor %}
</div> 

