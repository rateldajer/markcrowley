---
layout: page
permalink: /overview-decision-making/
title: An Overview of Decision Making Under Uncertainty Research
titleheader: An Overview of Decision Making Under Uncertainty Research
description: My own high-level view of decision making research papers.
topics: 
- decision-making
- mdp
- pomdp
- reinforcement-learning
- direct-policy-search
- value-function-approximation
nav: false
showtitle: true
aside: 
    toc: true
---

# TODO

- [ ] clean this up
- [ ] Create a higher level page for all topics, linking to these specific topic overviews. The gingko trees with topics in _this_week and in the RL course working notes will be the bases fr text in different pages. Maybe it should also be in a seperate GitHub repo which is editable by others? Or is it just my view? )my view) with hypothesis and other links
- [ ] Idea Tree
  - [ ] Artificial-intelligence
    - [ ] Machine-Learning
      - [ ] Deep-Learning
        - [ ] MLP, LSTM, CNN, Transformer
      - [ ] Tree-Based-Learning
      - [ ] Kernel-Learning
      - [ ] Manifold-Learning and Dimensionality-Reduction
    - [ ] Decision-Making (this page)
      - [ ] Reinforcement-Learning

## Main Ideas List

The main idea I wanted to write down was that there are many papers and topics in the database on this tree of topics:

- decision-making
  - [MDPs](#mdp) and POMDPs
  - Reinforcement Learning
    - Value Function Approximation
    - Direct Policy Search Methods
      - PPO
      - Actor-Critic

    - Model Free Value Based Methods
      - DQN
      - DPG
      - Actor-Critic

    - Model Based Methods





<b>Jump to Topic:</b> {% for t in page.topics %}<a href="#{{t}}">{{t}}</a> {% if forloop.last==false %} ~ {% endif %}{% endfor %}

*Note that papers will show up in multiple topics.*


<hr/>

# Topic List



<div class="publications">
{% for t in page.topics %}
  <h2><a name="{{t}}">{{t}}</a></h2>
  {% bibliography -f all-references -q @*[keywords~={{t}}]* %}
{% endfor %}


</div	>
