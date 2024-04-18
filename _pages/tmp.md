---
layout: page
title: people
titleheader: People in the Lab
permalink: /people/
nav: false
description: Information about current and former lab members. 
showtitle: true
---
	

<div class="projects grid">
  {% assign sorted_people = site.people | sort: "graduated" %}
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
