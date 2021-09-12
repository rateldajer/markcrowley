---
layout: page
title: Reinforcement Learning
name: Reinforcement Learning
permalink: /reinforcement-learning/
collection: keywords
keyword: reinforcement-learning
description: RL is the study of learning decision making policies from experience with computers.
publish: false
stage: field
showtitle: true
aside: 
    toc: true
---

## Testing Citations
Does the {% cite ref %} command work?


## Learning Resources
- The Textbook - http://incompleteideas.net/book/the-book-2nd.html
- [Martha White's RL Fundamentals Course](https://www.coursera.org/specializations/reinforcement-learning?utm_source=gg&utm_medium=sem&utm_content=04-ReinforcementLearning-UA-CA&campaignid=6770937312&adgroupid=85996872692&device=c&keyword=reinforcement%20learning%20course&matchtype=b&network=g&devicemodel=&adpostion=&creativeid=391979104237&hide_mobile_promo&gclid=Cj0KCQjwm9D0BRCMARIsAIfvfIYKjEq7S-DqrGVUNrH6GIcvwMRPX4tz_1LgKbgnt7nm2c-cvtAHy3YaAu9xEALw_wcB)
- [Sergey Levine's Deep RL Course](http://rail.eecs.berkeley.edu/deeprlcourse/)


### Seminal Deep RL Papers
- https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf

## Tools

- https://gym.openai.com/

<div class="publications">
  <h2>Our Papers on {{ page.name }}</h2> 
{% bibliography -q @*[keywords~={{page.keyword}} && self=1] %}
</div>

<div class="publications">
  <h2>Other Important Papers on {{ page.name }}</h2> 
{% bibliography -q @*[self=0 && keywords~={{page.keyword}}] %}
</div>

# TODO
- [x] add a bib wrapper from about to each page
- [ ] add a meta flag to "show bib" for the topic using the keyword field
- [ ] add all this to the page template
