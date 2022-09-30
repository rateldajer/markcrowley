---
layout: page
title: (draft) All the Keywords 
titleheader: All the keywords
permalink: /keywords/
nav: true
description: Trying to sort out all the different types of keywords. 
showtitle: true
---

todo: isn't there a page already somewhere with all the keywords/topics/methods/domains on all pages?


<h1>Topic</h1>
text


{% assign sorted_topics = site.topics | sort: "title" %}
{% assign keylist = "domains, methods, topics" | split: ", " %}
{% for topic in sorted_topics %}
   
<h3>{{ topic.title }}</h3>
{% for i in keylist %}
- {{i}} : {{ topic[i] }}
{% endfor %}
        
{% endfor %}
