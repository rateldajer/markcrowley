---
layout: page
title: people
titleheader: People in the Lab
permalink: /people/
nav: false
description: Information about current and former lab members. 
showtitle: true
showbib: true
---

  {% assign names = site.people | sort: "degree" %}
  
PEOPLE!: 

{{ names }}

{% for p in site.people %}
    {% for i in p %}
       {{i}} : {{ p[i] }} 
    {% endfor %}
print: {{ i }}
print: {{ p }}
{% endfor %}

<div class="projects grid">
  {% assign sorted_people = site.people  %}
  {% for person in sorted_people %}
      {% if person.output %}
          <div class="grid-item">
              {% if person.redirect %}
                  <a href="{{ person.redirect }}" target="_blank">
              {% else %}
                  <a href="{{ person.url | relative_url }}">
              {% endif %}
              <div class="card hoverable">
                {% if person.img %}
                <img src="{{ person.img | relative_url }}" alt="person thumbnail">
                {% endif %}
                <div class="card-body">
                  <h2 class="card-title">{{ person.givenname }} {{person.familyname}}</h2>
                  <p class="card-text">{{person.degree}} : {{ person.keywords }}</p>
                </div>
              </div>
            </a>
          </div>
      {% endif %}
{% endfor %}
</div>
