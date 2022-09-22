---
layout: post
date: {{date}} {{time}}
inline: false
description: Recently Accepted Papers
title: Three great papers accepted to AAAI, NeurIPS Workshop and EMBC in past month!
meta: publications
topics: marl, reinforcement-learning, deep-learning, attention-mechanism, mean-field-theory
domains: medical-imaging, video-games, planning
people: sriramganpathisubramanian, aishwaryaallada, kenminglee, markcrowley 
showdomains: true
showpeople: false
showbib: true
publish: true

---

Members of the UWECEML lab have had a good couple months, with a few notable papers accepted to great venues. 

## A New Approach to Scaling Decision Making to Many Agents

The most recently accepted paper {% cite ganapathisubramanian2022aaai
%} is a core topic in the final stages of my PhD student Sriram Ganapathi Subramanian into **[Multi-Agent Reinforcement Learning (MARL)](/marl/)**. 

In situations where the number of agents is very large, we need to make some assumptions about structure to make RL feasible. **[Mean Field Theory](/mean-field-theory)** is one such approach where each agent considers the impact to its interactions via another "cloud" agent which is actually an aggregation of all other agents, via a mean field calculation.

In this paper we relax a core requirement in existing Mean Field approaches which is that all agents use the same policy. Our new **Decentralized Mean Field Game** concept allows for agents to have separate policies but still use the mean field assumption about other agents to make decision making feasible. We show some convergence results for a provide a fixed point guarantee for a Q-learning based algorithm under this paradigm.

## Natural Language Analysis for Medical Reports

This paper {% cite allada2021embc %}, led by recently graduated student Aishwarya Krishna Allada, makes a comparative analysis of various natural language embedding models on the novel domain of digital pathology reports and attempts to determine the strengths and weaknesses of different ways of dealing with these large and variable language datasets. 

## Empirical Study of Reinforcement Learning Algorithms in Multi-Agent Settings

This study {% cite lee2021neuripsdeeprl
%} was led by fourth-year undergraduate student Ken Ming Lee with lots of guidance and help from my PhD student Sriram Ganapathi Subramanian. It's a great empirical comparison of a number of single-agent and multi-agent RL algorithms on a standard set of MARL problems. Often single-agent algorithms are quickly hacked in order to to decision making on multi-agent domains and seem to work fairly well. Our motivating question was how often is this true and what kinds of problems require approaches that consider more dedicated multi-agent interaction.









