---
layout: post
date: 2026-10-15
inline: false
title: "Paper Accepted at WACV 2027 on Empirical Auditing of Landmark Grounding in VLN"
topics: vision-language-navigation, robotics, machine-learning
tags:
- vision-language-action
- vision-language-navigation
- robotics
- large-language-models
- machine-learning
- multi-modal-data
people: joshqixuansun
published: true
output: true
showbib: true
showmeta: true
---

We are excited to share that our paper {% cite sun2027wacv %} has been accepted to the **Winter Conference on Applications of Computer Vision (WACV 2027)**!

Led by Ph.D. student [Josh Sun](/people/joshqixuansun) with help from all his coauthors, this work performs a kind of audit into whether existing **Vision-Language Action (VLA)** navigation models actually utilize the landmark instructions they are given rather than solving the task independent of those instructions.
If this seems like a strange question, think *groudning* as a kind of *allignment* question.
Measuring "performance" of the latest large-scale, language foundation models, whether they include vision inputs or not, is tricky for many reasons. 
Just one of those reasons is that these are very general pre-trained foundation models that are extremely effective at coming up with *adequate solutions to general requests* given their vast pre-training process. 

The allignment question here is whether the model's behaviour is *grounded* in the request we gave it. 
In other words, does it succeed at the task *because* of anything we told it or if it could have solved it with even less information? 
We have found that commong validation experiments don't always test whether the base model being used could solve things on its own. 

In this work we look at various ways to isolate what parts of the prompt and data given to the model were necessary and which were not. 
The result is somewhat surprising.

> {% reference sun2027wacv %}

Josh did a stellar job spearheading this project, building **LandMarkVLN**, a 7,228-sample diagnostic evaluation benchmark, and conducting rigorous visual interventions across eight released VLA models. 
Josh demonstrated that local navigation actions and visual sensitivity do not necessarily imply that VLA models rely on instructed landmarks, giving us crucial insights for building truly reliable embodied AI agents.

Josh will present the work at the WACV conference in Florida in January 2027.

