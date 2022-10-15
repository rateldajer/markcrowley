---
layout: page
permalink: 
title: Jekyll Tricks
description: useful tricks and shortcuts
nav: false
showtitle: true
---

<h2>two</h2>
<ul>
{% for t in site.data.coauthors %}
    <li> <a href="{{ t[1].url }}">{{ t[0] }}</a>
{% endfor %}
</ul>

<h2>three</h2>
<ul>
{% for t in site.data%}
    <li> <a href="{{t[1]['Crowley'].url }}">Crowley</a>
    <li> <a href="{{t[1].Crowley.url }}">Crowley</a>
{% endfor %}
<li> -{{ site.data.coauthors["Ganapathi Subramanian"].url }}-
<li> -{{ site.data.coauthors["Ganapathi Subramanian"]["url"] }}-
</ul>

<h2>Topic List</h2>
{% assign sorted_topics = site.topics | sort: "title" %}
{% for topic in sorted_topics %}
<h3>{{ topic.title }}</h3>
{% for i in topic %}
- {{i}} : {{ topic[i] }} 
{% endfor %}
- print: {{ topic }}    
        
        
{% endfor %}

<div class="publications by year">
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprints -q @*[year={{y}}]* %}
{% endfor %}

</div>
