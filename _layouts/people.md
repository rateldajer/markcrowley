---
layout: page
show_title: false
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
{% if page.linkedin %}
<li> linkedin: {{page.linkedin}}
{% endif %}
{% if page.website %}
<li> web: {{page.website}}
{% endif %}
{% if page.status %}
<li> status: {{page.status}}
{% endif %}
</ul>

{% if page.content %}
{{ content }}
{% endif %}

</div>
