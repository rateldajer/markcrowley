---
layout: page
permalink: /preprints/
title: recent preprints
description: Preprints and Working Papers
years: [2026, 2025, 2024]
nav: false
showtitle: true
---

Also see:
- [All Published Works](/publications)
- **[Selected Showcase Publications](/showcase)**
- [Publications Grouped by Research Topics](/pub-by-topic/)
- [Defended Theses from the Lab](/theses)
- [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ)
- recent preprints
    - [My Arxiv Preprint Page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M)

Note that this list may not be updated as frequently as others, see [my Arxiv page](https://arxiv.org/search/cs?searchtype=author&query=Crowley%2C+M) and [Google Scholar](https://scholar.google.ca/citations?user=eL_y80EAAAAJ) for the latest.

<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>
