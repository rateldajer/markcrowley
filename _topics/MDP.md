---
layout: page
title: Markov Decision Processes
permalink: /mdp/
name: MDP
collection: keywords
keyword: MDP
description: Markov Decision Processes (MDPs) are a mathematical language for definiing the problem of making decisions over time using only the current observations and knowledge.
publish: true
stage: method
showtitle: true
aside: 
    toc: true
---

## Our Papers on {{ name }}
{% bibliography -q @*[keywords~=MDP && self=1] %}

## Other Papers on {{ name }}
{% bibliography -q @*[self=0 && keywords~=MDP] %}


