---
layout: page
show_title: false
social: false
---
<div class="post">
  <header class="post-header">
<h1 class="post-title">
{{ page.givenname }} {{ page.familyname }}  ({{ page.degree}})</h1>
  </header>

<ul>
{% if page.img %}
<li> image - {{page.img }}.png
{% endif %}

<h2>Links</h2>
{% if page.website %}
<li> web: {{page.website}}
{% endif %}
{% if page.linkedin %}
<li> linkedin: {{page.linkedin}}
{% endif %}
{% if page.status %}
<li> status: {{page.status}}
{% endif %}
</ul>

| Degree | Status | Keywords |
| ----- | -----  | -----  |
| page.degree | page.status | page.keywords |


{% if page.status == "graduated" and page.thesiskey %}
> {% reference page.thesiskey -f theses %}
{% endif %}

<h3>thesis as bib</h3>
{% bibliography -f theses -q @*[author~={{ page.familyname }},status^=1]* %}

<h3>Content</h3>
{% if page.content %}
{{ content }}
{% endif %}

</div>
