---
layout: post
date: 2022-09-12 15:41:00-0400
inline: false
description: Lab News for Sept 2022
title: Lab News - PhD Defense, papers, jobs
meta: publications
topics: marl, reinforcement-learning, deep-learning, mean-field-theory, empirical
domains: forest-management, ai-for-games
people: sriramganpathisubramanian, kenminglee, benyaminghojogh, markcrowley 
showdomains: true
showpeople: true
showbib: true
publish: false

---

Members of the UWECEML lab have had a great couple months, with some nice a publications and lots of career news.

## Publications

### A New Approach to Scaling Decision Making to Many Agents

The most recently accepted paper {% cite ganapathisubramanian2022aaai
%} is a core topic in the final stages of my PhD student Sriram Ganapathi Subramanian into **[Multi-Agent Reinforcement Learning (MARL)](/marl/)**. 

In situations where the number of agents is very large, we need to make some assumptions about structure to make RL feasible. **[Mean Field Theory](/mean-field-theory)** is one such approach where each agent considers the impact to its interactions via another "cloud" agent which is actually an aggregation of all other agents, via a mean field calculation.

In this paper we relax a core requirement in existing Mean Field approaches which is that all agents use the same policy. Our new **Decentralized Mean Field Game** concept allows for agents to have separate policies but still use the mean field assumption about other agents to make decision making feasible. We show some convergence results for a provide a fixed point guarantee for a Q-learning based algorithm under this paradigm.


### Empirical Study of Reinforcement Learning Algorithms in Multi-Agent Settings
#todo journal paper published
{% cite lee2021frontai %}


This project was led by fourth-year undergraduate student Ken Ming Lee with lots of guidance and help from my PhD student Sriram Ganapathi Subramanian. It's a great empirical comparison of a number of single-agent and multi-agent RL algorithms on a standard set of MARL problems. Often single-agent algorithms are quickly hacked in order to to decision making on multi-agent domains and seem to work fairly well. Our motivating question was how often is this true and what kinds of problems require approaches that consider more dedicated multi-agent interaction.

This work expands on a previous study {% cite lee2021neuripsdeeprl %} from a NeurIPS Workshop in 2021. 





## Lab Member News

### Sriram's Defence
On (date) long-time lab member Sriram Ganapathi Subramanian successfully defended his PhD thesis: "Multi-Agent Reinforcement Learning in Large Complex Environments"

> \cite{subramanian2022uwspace}

Congratulations Sriram!

Sriram started a postdoc position at the Vector Institute in September 2022 working with Prof. Sheila Mcllraith at UofT and Prof. Pascal Poupart at UWaterloo.


### Benyamin Ghojogh
Former PhD student Benyamin Ghojogh has taken up a new position at *Research Associate at KisoJi Biotechnology* working on exciting research on
> We are working on developing AI tools for paratope-epitope interaction prediction, such as Machine Learning methods to describe VHH Antibodies for semantic clustering, selection, and matching. We aim to expedite the drug discovery process through the in-silico methodologies.

Can't wait to hear more Benyamin!

### Promotion to Tenure
As of July 1, 2022, Dr. Mark Crowley is now a tenured, Associate Professor in the ECE department! Phew.
