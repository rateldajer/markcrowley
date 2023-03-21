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
- **[Selected Showcase Publications](/showcase)**
- [Publications Grouped by Research Topics](/pub-by-topic/)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)



Note that this list may not be updated as frequently as others, see [my Arxiv page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M) and [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ) for the latest.

<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>
