---
layout: post
title: RLDM 2019 Conference Summary
name: RLDM 2019 Conference Summary
tags: reinforcement-learning, conference-summary, reinforcement-learning, conference-summary
description: I attended the fourth bi-annual RLDM conference in Montreal in July 2019, these are some notes I took.
showtitle: true
date: 2019-07-25 21:01:00
showtopics: true
aside: 
    toc: true
---

# Reinforcement Learning and Decision Making Conference

The fourth iteration of this conference was held in Montreal July 7-10, 2019.


## Basic Information

- Conference Website: http://rldm.org/
- Conference Brochure: http://otto.lab.mcgill.ca/temp/RLDM2019ProgramBrochure.pdf
- A PDF of all abstracts accepted: http://rldm.org/papers/abstracts.pdf

[TOC]

# Neuro Intro Tutorial 

*Melissa Sharpe , UCLA* 

## Associative Tasks

These are well established theories on associations by tasks to brain. She uses it to test computational questions about behaviour.

## Associative learning 

The main principle of association between actions and rewards based on Pavlovian conditioning.
**Example: Rats** sound tone associated with food

**Prediction error:**

- if they associate soured with food turds, add light they don't learn it
- they only learn when their are error, in predictions
- leads to causal learning, correlation isn't enough 

## Two forms of learning (conditional reinforcement):

- value of tone itself : like watching cooking show
- value of a *causal outcome* of the reward (food):
  - this shows up after the signal (tone)
  - This explains some of the irrational behaviour of drug users. Signals

## Neutral Associations

Rats can learn to associate sound + light (sensory prediction). Later when they learn that sound leads to food then they'll *infer that light leads to food too*. But the way they *value the light and the sound themselves* will differ!:

- They will happily press a button to hear the bell even though they know they are full and don't want food. They might even "enjoy" hearing the bell because it reminds them of food.

- But the light, which is also associated by inference to food arriving, doesn't hold any value. They won't press the button to see the light.

- The order they learn about the light+sound and about the food, makes a difference here too!

  

## Questions

- so are there completely diffenet learning (conditioning)
some types of learning associate value in itself and others are just about prediction and causation?
- are these results arising from particular brain structures or an algorithm? *Is there even a difference?*

# Dopamine Prediction Error

(Schultz 1997 papers)* - the discovery of it is really interesting through the 90's as a story of scientific discovery

Dopamine neurons encode suprise and cause learning:
- once the association is learned then when it predicts reward the dopamine fires anyways. 
- If no reward also encodes dissapointment
- They linked this to TD(0) learning
- So dopamine is temporal difference value

Optogenetics are used now to validate this

- then can explicitly send TD errors into dopamine neurons and see effect
- it's like adding suprise even when they aren't suprised , or increasing the reward even though its the same food
- if they kill off dopamine entirely the rats do still learn, but it's reduced
- they also show it encourages sensory specific situations, so Q(s, a)

There are subtle differences in how dopamine effects associating value to stimulus and learning causal relations
- the timing of when the dopamine armies seems to matter
- so small changes in when and how much d. p or reward is recieved can lead to huge differences.



# Dynamic Decisions in Humans

*Cleotilde Gonzalez , CMU*

## Irrationality : how should we define it?

Whenever we do not choose the action that maximizes our reward based on or model of the world-values. Framing bias is relevant.

## Naturalistic Decision Making

*C. Klein, Oksana., Klinger*

- human factors and ergonomics
  - how-do people really make decisions
  - expert decision makers, so quite rational but lots of knowledge ahead
    time sensitive, huge messy domains
- Some conclusions:
  - expert decision amkers often *know* what to do, they don't feel they really make a decision choice in the classical sense
  - if experience doesn't provide solution then they give up
    and run forward a simulator in their head based on experience
    - tree search? MCTS? UCB?

## Dynamic Decision Making (DDM)

They use the idea of decision makers who are experts in complex noisy domains but carried out in lab experiments with more control. This includes closed loop Decision making

**Properties of DDM:**

- utility can be dependent on the
- decisions overtime are interdependent
- limited time and cognitive resources
- delayed feedback

**Two Types:**

- choice - maximize total reward
- control-maintain system balance

### Consequential choice Problems

These are choices which are important and cannot be rolled back (eg.  forest fire, finance)

### Choice from Sampling

Choices can be tried with no impact before a real consequential choice is made (eg. shopping for clothes)

##Control

The goal is to maintain a particular state of a 'stock' (eg. weight, temperature in environment)

##Post office / Water Flow Microworld

*(Gonzales, Hunan Factors, 2004)*
They get people to play these very challenging games
then analyse their strategies and heuristics they use 

## Questions Arising from their Work

**1. How do memory and intelligence affect this?**

- highly skilled people leave regardless
- low skilled people give up an rely on 'advised heuristic as time goes on

**2. Does practice under time pressure help?**

- No . People who learn with no time pressure learn better and perform better under time pressure
- learn slow, play fast
- learner who had more time are more willing to ignore simple heuristic advice once they master it

**3. Does more practice help?**

- Practice doesn't help under time pressure but in slow learning it helps a lot to be robust.


##Instance Based Learning

![20190707_160550](/Users/mcrowley/Downloads/rldm2019/20190707_160550.jpg)*(Gordon, Lerch and Le biene, 2003)*

## ACT-R 

*(Andersons Lebiere, 1998)* 

A model for combining Memory and Symbolic representations and how it happens in the human mind.

### Description-Experience Gap

*(Hertwig, 2004)*

- the experiment is like a simplified Multi-armed Bandit task carried out on people
- Theydiscovered an interesting effect in human decision making



#### Description:

- you tell them the probabilities
- people overweight unlikely situations, Prospect Theory

#### Experience:

- when people build their estimates from actual experience
- then they don't behave that way because ' under weight unlikely situations
- So Prospect Theory only seems to apply to how people apply probabities that are described to them

##IBLT

- create new meta states, "instances", to evaluate based on multiple memorized events that are similar to the current situation
- they have a Python library to define their models

# Counterfactual RL

[Emma Brunskill](https://cs.stanford.edu/people/ebrun/)

*Also Check out her [awesome tutorial](awesome tutorial) on RL for the people which gives a great top-to-bottom perspective on the current state of RL.*

# Counterfactuals

*Emma Brunskill*

How do we focus is on treating learning concepts as RL?
She says **Counterfactual learning** is related to Batch learning and experience replay since both are learning based on old data.
We can't know what would have happened with different choices

```
 "The ability to imagine what would have hopped is critical to human intelligence." - Judea Pearl
```

## Batch Policy Optimization

![20190707_165441](/Users/mcrowley/Downloads/rldm2019/20190707_165441.jpg)

## Policy Evaluation

TODO: Importune Sylyfr RL Policy Eva#

(Preap, 2. ⇒

weighting the trajectories using just a combination of the policy probabilities
see this, high variance

*Stationary Importance Sampling (Challah and Manornor 2017)*

- This is a new method that has lower variance than original approach
  but is still hard to estimate.


##Interesting Idea Related to Policy Optimization

If your state representation is *too simple* for the domain then the problem is *no longer Markov*. This is because you'll need to remember past states to compensate for the lack of representation. This is the flip side of the usual idea that *everything is Markovian* as long as you have rich enough features in your state description.

So, if your models are bad then picking the MLE for the dynamics isn't a good idea
even using importance sampling has problems because it can have very high variance even though it isn't biased.

##A Big Idea

Unlike in supervised learning these are really hard in RL:

- structural risk minimization

- cross validation

  

![20190707_174155](/Users/mcrowley/Downloads/rldm2019/20190707_174155.jpg)

There are promising methods for dealing with this in non i. i. d. domains but it's hard.

## Moving the Goalpost

### Direct Batch Policy Search

- doing policy gradients while using old data
- traditional approach for this leads to very high variance
- use importance sampling to reweight old trajectories and still converge

![20190707_174918](/Users/mcrowley/Downloads/rldm2019/20190707_174918.jpg)
  *(Liu, Swaminathan UAI, 2019)*

###Finding the Best Policy in a class

- they have a result for doing this using an advantage function
- restricted to domains with a single "when to act = decision (eg. when to start a drug treatment, when to sell a stock)
- one advantage of this is interpretability since plicies are more related to the actual human experience.

# Distributional Reinforcement Learning

*Will Dabney, DeepMind*

## History

- discovering TD leraning for AI methods
- then discoering that this looks similar to what happens in the brain with dopamine neurons
- estaimtes of value at all states udpated in direction of improving prediction error

## Distributional TD Learning

- traditional TD learning updates for all states (or neurons) with the same scale
- but in DTD they weight the updates using the local distribution of rewards somehow
- switch from mean value update to distributional value update
- they find that it seems like learning the distribution helps to learn a better representation

## Validation with Simple Experimental Tasks with Animals

- animals receive one of seven amounts of food, with a prob distribution
- some animals get a signal associated with each case
- traditional TD learning: if reward is above average the positive learning happens
- but what about the distribution for each neuron / state?
- looking at experimental data it seems to align with what we'd expect from a distributional model rather than the old mean approach



# Count-based Exploration with Successor Representation

*Marlos Machado, Michael Bowling*

## Successor Representation

- Function approximatoin requires that we really see examples of the different state we want values of. If we never see then then we can't learn it.
- one simple wayt o bootstrap this is useing proximity between states.
- but proximity can break in spatial domains or complex state spaces.
- what we really want is to talk about how many steps it would take to get between two 'nearby' states rahter than their euclidean distance
  
  

## Counting the number of visits to a state along a trajectory

- this can be estimated with TD learning
- there is a good way to do function approximation on this as well
- The Success Representation (SR) naturally comes out of a the dual approach to dynamic programing for RL
- there is also some evidence taht it matches some of what is happening in the hippocampus
- this can be seen as an alternative to optimism under uncertainty used in R-Max and others

## Updating Existing Algorithms

- add the L2 norm of the SR as an exploration bonus to standard SARSA
- **intuition**: if some state has not been visited much before it will get a bonus to encourage exploring it
- huge improvement on SARSA
- also works to add it to model based algorithms like $E^3$, R-MAX etc

## Function Approximation

- adding this idea to DQN seems to help as well especially for domains for random exploration doesn't work well

## Result

Using the norm of the successor representation encodes state visitition counts and helps to explore faster.

# Directions in Distributional Learning

*Will Dabney, Deep Mind*

Another talk on this approach in general.

- Distributed RL says we should learn the true distribution of the values.
- The means can be used directely to update value estimates using the bellman equation.
- But this doesn't work if you aren't using the mean (moments) because there may be multiple distributions that are consistent with that mean.
- So the big question is how to best impute the right distribution to explain the experiences. 
- The way they've approached it is to fix the representation or projection to a consistent estimator and preserves the mean even though it's not necessarily the best one.

## The Big idea 

Treat the return itself as a random variable. this will have the same recursive structure as the bellman equation except it is the relationship between a distribution over rewards and the valeu distribtuion.

### Why does Distributional RL Work?

- helps maintain stability  for complex domains for deep RL
- aids representation learning by providing a stronger signal about the structure of the domain
- it helps with improving generalization error, that is learning on some states can work well in very different unseen states, which can be shown to really help with improving performance in RL.

### The Virtuous Circle of RL

- see *"Neuro-science Inspired AI"* article by *Demis Hassabis of Deep Mind*.
- The communication between cognitive science, psychology, neuroscience and CS/AI helps us all to learn useful things and contribute to the overall truth

### Further Reading 

- *Marc G. Bellemare, Will Dabney, Rémi Munos. 2017.*
  https://arxiv.org/abs/1707.06887
- Deep Mind 2019 Arxiv:
  - DRL algorithms can be decomposed as the combination of some statistical estimator and a method for imputing a return distribution consistent with that set of statistics
  - https://deepmind.com/research/publications/statistics-and-samples-distributional-reinforcement-learning/

# Substance Use Disorder

*Anna Konova*

Drug users seem to be risk seeking so their team modelled ambiguity as *risk tolerance* separately to explain people's varying values for money and drugs ambiguity tolerance. They founds this explains ongoing drug use better than risk tolerance.

# Hyperbolic Discounting

*William Fedus, Yoshua Bengio — Google Brain*

- The standard $\gamma^t$ discount factor is an exponential discounting
- $\frac{1}{1+kt}$ is a **hyperbolic discount**
- *(Souzo, 1998)* use survival (t) rather than $\gamma^t$ 
  - the probability of surviving until timestep t
  - we can derive standard $\gamma^t$ from this for a domain with a fixed risk of dying at each step
- but if the hazard rate depends a state we get other discount functions
- they simply the use of this by training the agent on multiple time horizons as an
  auxiliary task
- this is part of a larger discussion in RL that the common assumptions about the du't work

# Heart Health with RL

*Susan Murphy*

**Goal:** Promote behaviour changes on taking medication, reducing addiction etc.

Existing health support apps take two main forms:

- *pull* : just info, depends on user
- *push*: deliver intervention when needed

## Heart steps app

An advisor app to help encourage sedentary people at risk of heart attacks.
Very customized to personal schedule and context.

They tried to build an RL agent to push messages but not have the person get used to it.
This problem has interesting challenges:

- very noisy data, unknown variables, complex rewards
- delayed penalties (over seasitivation)
- immediately all actions are positive 

## Questions:

Can they reuse previous trajectories?

# Termination Critic

*Anna Harutyunyan, Doina Recep,  Remi Munos, et. al. (DeepMind)* 

## Temporal Abstraction

Reasoning at multiple timescales

- We can remember and reason about different levels of detail over time.
- why do we do it? The hope is that high level plans are more reusable.

How do we define and measure generalization? How do we encode inductive biases?

 ## Options

**option(O) = policy($\pi$) + termination condition $\beta$**

Traditionally, policy is the focus, but termination also optimizes the same thing. Biases are added in to encourage options to last longer.

**Their idea:** a separate termination rule to be focussed on when to end option entirely.

###Option Transition Model

- this is an MDP where we take options instead of actions
- provide a distribution over all states you could end up in
- however still need to learn the per-step Beta parameter
- they show how you can define the value function and Bellman equation for Beta then they can solve this with policy gradients.

**Constraints on Options:** The goal is the encourage options to be simpler. Minimize entropy offinal option model.

**Termination critic:** They use the *Actor-Critic* approach but have a critic for the termination rule in addition to the policy.

# Intrinsic Motivation (a.k.a Curiosity)

*(Pierre-Yves Oudeyer , INRIA)*

Their lab look at intrinsic motivation in humans and machines. They explore developmental learning in children and try to apply it to 

- building robots
- developing better education methods

It is well known that children always explore and invent their own goals. So looking only at the accuracy statistics is not useful, instead we need to consider the context.

##The Learning Progress Hypothesis

"Interestingness" is not just about novelty or surprise.
It is about situations where a high level of learning is happening. If something becomes partially mastered then progress will slow and agent/child should/will lose interest.

## IAC Algorithm

*(Oudeyer, IEEE TEC 2017)*

- Build an interesting mess metric using *change in gradient* during learning for many points in state-action space.
- Choose actions to try which high values of this metric are best.
- Hierarchically divide the space into distinct regions by clustering on the metric.

They also explore the use *Inverse Reinforcement Learning*

*(Forester et al. 2017)* have a great video of robot learning.

# Anatomy of a Social Interaction

*Luke Chang*

They look at actual human social interactions for compelx dynamics between choices amongst multiple people.

## Trust Game

- sequence of choices: join or don't join the interaction
- share of don't share : information

### Prediction Error in the Brain

- they found correlations between activations in part of the brain related to prediction error
- they performed user study on trust game where people play with agents who have trustworthyness probabilities rather than actuall people
- they scanned people's brains during playing the game to see what lights up in the brain
- **result**: values are higher when interacting with someone you trust

### What makes someone trustworthy?

- Recent study on Trust around the world, lost wallet game [Cohn et al, 2019, Science](https://www.nytimes.com/2019/06/20/science/lost-wallet-what-to-do.html)
  - that study found that people are more likely to return the wallet if there was a lot of money in it. 
  - Economists think there is not existing theory to explain this
- Psychological Game Theory can explain this
  - one agent has *second order* theory about other player and they converge on a solution 
  - this involves thikning about the dissapointment the other person is going to experience and this is partially valid. If the money is higher obviously this weight is higher.
  - [TODO](TODO): see image
  - They also find support for this by looking at brain scans

## Moral Strategy Model
![20190709_144501](/Users/mcrowley/Downloads/rldm2019/Photos/20190709_144501.jpg)



## Theory of Mind

Many existing modles of theory of mind are low dimensional, a few main types of quealities and that they are static over time.

There is a push to explore this using *Inverse Reinforcement Learning* and *Bayesian Learning*

### Prediction Game

- goal is for player to learn the likely straggy of another player from overseved actions
- people can predict very quickly what watching people will do
- RL doing it to optimaize doesn't do well
- but IRL does better than RL here
- IRL does not perform as well as humans
- Also, this domain gave the IRL learner a lot of state representation information which humans don't have

## Guilt Aversion as a Useful Component of Values

- It's important to include guilt or theory of mind about other's dissapointment or pain
- It is a real effect in human decision making and it is robust across culture and does not conform to the standard economics idea of expected utility maximization
- Advice being given for medical and other safety-critical domains needs to consider this.

# Learning to Learn to Communicate

*Abhinav Gupta, Joelle Pineau, et al.*

Learning of simulated languages between agents including programming language, natural or artificial ones.

Interesting work that explicitely builds compositional models of agents learning languages so that they contain some of the properties of natural languages.



# Arbitration between imitation and emulation during human observational learning

*Caroline J Charpentier; Kiyohito Iigaya; John O’Doherty*

Learning by observing people perform a tasks, there are two main approaches:

- imitation learning
- learning by inferring about tier goals and preferences

**Question:** do people alternate between these two strateies and when?

**Experiment:**

- bandit task to choose which to pull, some feature about hte machines to identify them
- you get to watch another player follow a straegy and you know they are a good player
- you also know that one of the features (tokens) is perfectly correlated with high reward

**Hypothesis:** 

- immitation is slower to learn, but better when system has lots of uncertainty
- emulation will be favoured for highly volatile domains

**Results:**

- people use both approaches

## Computational Models

- they build a computational model for each strategy and an arbitration model which weights a tradeoff between the two strategies
- they show the arbitration model performs better
- then they test if it explains the human behaviour better and they find it idoes very closely

## Implications

- they perform fMRI scans and show which parts of the brain correlate with activity for each of the two strategies and the joint arbitration signal too



# Can a Game Require Theory of Mind?

*Michael Bowling*

Game: ***Hanabi*** - Michael explained how this card game blends the notion of communication between explicit messages and observation of the actions of other players

# Working Memory

*speaker*

Working Memory is fast to use but has limited capacity and is forgotten quickly.

## Simple Experiment

Give people a small set (3-7) of images to remember the position of based on another larger image with stimuatus in it.

Try to test two aspects of working memory if it is an RL system

- time limiting factors, how long it lasts
- Size of memory, how many different elements can be remembered

### Results

People can perform optimally, but once it gets to 5 or 6 they start having 20-30% errors. But the RL model alone of memory doesn't have these problems.

### Adding a Seperate Working Memory Process

RL alone isn't enough, so we need some kind of mixture model. Once this is added then the model corresponds closely to human performance.

## But...Working Memory Interferes with RL

How do WM and RL interact?

- EEG studies show that RL reward prediction or reward history are correlated with the set size (the number of things trying to be remembered). So they are not independent. So WM is somehow blocking?
- EEG studies also show that the Q-value drops faster (improves faster) for small sets, so somehow WM is helping?
- Long term associations are learned better (this is harder) when the set of images is larger.

### So What's Happening?

WM blocks RL by contributing to the reward prediction error and helping improve it, there is a closed loop between them.

## Why is  this Important?

Keeping an open mind about how different observed brain systems could contribute to and interact with learning. Example domains help to motivate this:

- Schizophrenia
  - They can show that working memory is impaired in Schizophrenia patients and that it is due largely to WM problems seperated from RL, this is only visible if WM is modelled explicitely.
- Age related learning
  - they found that learning rate seems to increase with age to compensate with decrease in working memory

There has been a lot of success in Cognitive science and neuroscience to grab useful ideas from CS RL to do more experiments. She encourages the CS RL community to grab more ideas from neuroscience and try them out in computational models, working memory for example seems to have benefits beyond benefits to RL alone.

# Reinforcement Learning for Robots

*Chelsea Finn, Berkelty, Google Brain, Stanford*

A nice aspect of doing RL on robots is that you can't get around the problems of noise, bad reward models, generalization as you can in simulation. A major problem right now is training specialist robots is known but they generalize very badly even on mundane differences. So **exploration**, using **raw sensory input** and **continual improvement without supervision** are needed.

## Learning Reusable Models from Self-Supervision

Their approach (**Visual Foresight**) is to do two things

- Learn general policies through unsupervised exploration
- Learn fundamental physics and dynamics from pre-existing videos

Their state representation model is the full images that the robot sees, this includes all the pixels and the view of the environment. So their dynamics prediction needs to be a Recurrent Neural Network that predicts video images.

# How We Know When Not to Think

*Fiery Cushman*

A standard dichotomy is **Model-based (Habitual) vs Model-based (Planning)**

How can a little bit of model-based knowledge help with planning?

- this is important because in reality we have an inifinity of choices and yes we only consider a small subset, how does that happen?
- **consideration set** - things we usually want to consider for this task, feasible options, but very restricted
- **choice** - this is the standard onine- value based estiamtion usin g amodel to pit the best thing for the context

They show a bunch of experiments highlights that people are able to seperate these two tasks well. They find that the consideration set generally based on a quick heuristic of pre-cached cases weighted by value. This means we think of things based on value, even if we need to eventually choose amongst that set according to something other than value maximization (e.g. choose your least favourite food, choose an item that satisfies some convoluted constraint.)

## What does "Possible" mean?

We usually mean practical when we say possible, not if it is physically conceivable. They show some interesting experiemntal results that show immoral considerations are not immediately added to these consideration sets, but only available under more deliberation. So we don't even consider these scenarios to save time.

One final result is that this indicates that 

# Play : Interplay of Goals and Subgoals in Mental Development

*Rich Sutton*

We finally wrapped up with a talk by Rich Sutton himself. He argues for there being an truly Integrated Science of Mind that applies equally to *biological* and *machine* minds.

```
Intelligence== Mind - Rich Sutton

```

### The Reward Hypothesis is great but...

- it reduces the importance of subgoals
- it seems to be something that can't change over time

## Where are we?

We start with goals :

- first we learn value functions based on expected future reward
- we learn policies

Next we need to look at subgoals:

- learn about state - eg. state representations
- skills - eg. options
- models - 

These are all *subproblems* that are not essentially about reward or value. How do we learn them or represent them generally?

He thinks **play** is an important way to look at it.

Three key open quetsions about subproblems in RL:

1. Q1 - what should subproblems be
2. Q2 - where do they come from
3. Q3 - how do subproblems help the main problem (ie. how to subgoals help the main reward maximization task)
	- Learning to solve subproblems could help with shaping better *state representations*, *behaviour patterns* that are more coherent
	- It also allows *high level planning* because now you have a mdoel of what happens after you've achieved the subgoal


Some settled issues:

- subproblems are a reward in themselves an dmay be terminal, planning stops
- solving a subproblem can be done with an option, a seperately subpolicy 

![20190710_113310](20190710_113310.jpg)

![20190710_114403](20190710_114403.jpg)



That's All, it was fun. See you in two years at Brown!

