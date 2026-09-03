---
layout: post
date: 2026-08-22
inline: false
title: New Journal Publication on Causal Representation Learning
topics: deep-learning, causality, machine-larning
tags:
  - machine-learning
  - machine-ethics
  - causality
  - representation-learning
people: shayan
published: true
output: true
showbib: true
showmeta: true
---

We have an exciting new journal publication {% cite bagi2026springermlj %} based on the work of former PhD student <i>Shayan Shirahmadi Gale Bagi</i>, along with Professors Zahra Gharaee and Oliver Schulte. The paper can be found in the latest issue of **Nature Machine Learning**

> {% reference bagi2026springermlj %}

This paper falls into the general research topic is *[causality](/causality/)*, including *modeling, representation, learning about causal relations*, which was the core of Shayan's PhD thesis.


Shayan defended his thesis in 2025 {% cite bagi2025uwspace -f theses %} and now works at Huawei Canada as an AI Engineer.
His thesis work was on theoretical and applied methods for improving our ability to learn latent causal relationships from observational data. 
This included a paper <a href="https://proceedings.mlr.press/v202/shirahmad-gale-bagi23a.html">"Generative Causal Representation Learning for Out-of-Distribution Motion Forecasting"</a> at ICML in 2023 {% cite bagi2023icml %}.
In that paper, Shayan proposed a new framework for leveraging causal information to improve robustness of learning in the presence of distribution shift and included. Empirical results on the motion forecasting domain support the theoretical findings.

The current paper expands on some of the final insights in Shayan's thesis about learning causal representations from data without access to ground-truth causal graphs, which presents a difficult challenge in representation learning. 

Implicit approaches—where the model learns causal dependencies without explicitly parameterizing the causal graph—offer a compelling advantage over explicit methods by avoiding optimization difficulties such as local minima associated with adjacency matrix estimation. However, existing implicit methods often assume access to hard interventions, which are rarely feasible in real-world scenarios. 
In contrast, soft interventions—more prevalent in practice—modify causal mechanisms without severing parental dependencies, introducing subtle, ambiguous effects that confound learning. 

To address this, this paper introduces **ICRL-SM**, a novel method for **Implicit Causal Representation Learning from Soft Interventions using a causal Mechanism switch variable**. This variable captures unwanted changes induced by soft interventions, enabling the model to focus on the necessary variations that reflect underlying causal structure. Our framework leverages a variational autoencoder trained on paired pre- and post-intervention samples, and is theoretically grounded under a set of assumptions that ensure identifiability of causal representations. Although some assumptions (e.g., Gaussianity of latent variables, diffeomorphic decoders) are strict, we show empirically that our method performs robustly even when these are violated—demonstrating strong results on both synthetic benchmarks and real-world image datasets. These findings highlight the potential of ICRL-SM to bridge the gap between theoretical identifiability and practical applicability, advancing causal representation learning under realistic conditions. 

**Source Code:** The [source code](https://github.com/sshirahmad/ICRL) for this paper is available at: [https://github.com/sshirahmad/ICRL]



