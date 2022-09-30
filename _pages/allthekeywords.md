---
layout: page
title: (draft) All the Keywords 
titleheader: All the keywords
permalink: /keywords/
nav: true
description: Trying to sort out all the different types of keywords. 
showtitle: true
---


{% assign sorted_topics = site.topics | sort: "title" %}
{% assign keylist = "domains, methods, projects, topics" | split: ", " %}
{% assign showlist = "showbib, showdomains, showfields, showmethods, showpeople, showprojects, showwebpage, publish, output" | split    : ", " %}
{% assign fieldlist = "path, url, description, collection, categories, domains, methods, projects, topics" | split: ", " %}
{% assign itemtypelist = "pages, posts, courses, news, projects, topics, oldprojects" | split: ", " %}

{% for itemtype in itemtypelist %}
<h1>{{ itemtype }}</h1>
<hr>
{% assign sorted_items = site[itemtype] | sort: path %}
{% for item in sorted_items %}
<h2>{{ item.title }}</h2>

{% for key in fieldlist %}
- {{ key }} : {{ item[key] }} 
{% endfor %}
{% for i in showlist %} | {{i}} {% endfor %} |
{% for i in showlist %} | ---  {% endfor %} |
{% for i in showlist %} | {{ topic[i] }} {% endfor %} |
{% endfor %}
{% endfor %}

