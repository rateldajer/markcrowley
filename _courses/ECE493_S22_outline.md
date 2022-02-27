---
layout: page
description: Spring 2022 - ECE 457C
permalink: /rlcourse/
title: Reinforcement Learning
img: /assets/img/teaching/ece493-logo.png
date: 2022-02-26
meta: ECE 457C - Spring 2022
nav: false
showtitle: true
importance: 1

---

***Note:*** *This course was formerly known as "[ECE 493 Topic 42 - Reinforcement Learning](/rlcourseS21/)"*

| **Next Offering:** Spring 2022            | **Instructor:** Prof. Mark Crowley                                                               |
| :---:                                     | :---:                                                                                            |
| [Old Spring 2021 Website]( /rlcourse21/ ) | [Updated List of Resources and Links](https://gingkoapp.com/course-457c-links-for-students)  |
| Piazza Discussions (TBD)                  | [Course YouTube Channel](https://www.youtube.com/channel/UC6p1AJ7jKNFp6OB2MmAoWvA) |



### Course Description

Introduction to [Reinforcement Learning](/reinforcement-learning/) (RL) theory and algorithms for learning decision-making policies in situations with uncertainty and limited information. Topics include Markov decision processes, classic exact/approximate RL algorithms such as value/policy iteration, Q-learning, State-action-reward-state-action (SARSA), Temporal Difference (TD) methods, policy gradients, actor-critic, and Deep RL such as Deep Q-Learning (DQN), Asynchronous Advantage Actor Critic (A3C), and Deep Deterministic Policy Gradient (DDPG).



### Required Background

The course will use concepts from ECE 203 and ECE 307 on Bayesian Probability and Statistics, these will be reviewed but familiarity will help significantly. All other concepts needed for the course will be introduced directly. Examples, assignments and projects will depend on programming ability in Python.



## Course Learning Objectives and Topic Details

### Learning Objectives
This course complements other AI courses in ECE by focussing on the
methods for representation and reasoning about uncertain knowledge for
the purposes of analysis and decision making. At each stage of the
course we will look at relevant applications of the methods being
discussed. 

For example, in 2016 the AI program "AlphaGO" defeated human world class
players of the game Go for the first time. This system requires many
different methods to enable reasoning, probabilistic inference, planning
and decision optimization. In this course we will build up the
fundamental knowledge about these components and how they combine
together to make such systems possible.

1. Identify and Explain the component theoretical concepts of Reinforcement Learning systems.
2. Implement or instantiate using a library any of the core Reinforcement Learning algorithms on a variety of domains. 
3. Evaluate the performance of a particular RL system on a given domain through proper experimental design, statistical analysis and visualization.

### Topics
1. Motivation and Context
   - Importance of reasoning and decision making about uncertainty.  
   - Connection to Artificial Intelligence and Machine Learning.
   - Probability review.
2. Decision making under uncertainty: 	 
    - Multi-Armed Bandit (MAB) problems, Thompson Sampling.
    - Markov Decision Processes (MDPs), Influence Diagram representation.
3. Solving MDPs
   - Theory, Bellman equations
   - Relation to Control Theory
   - Value Iteration, Policy Iteration
4. The Reinforcement Learning Problem
   - Approximately solving MDPs by interacting with the environment
   - SARSA algorithm
   - Q-learning algorithm
5. Temporal Difference Learning
   - Eligibility Traces
   - TD(𝜆) 
6. Direct Policy Search
   - Policy Gradients methods
   - Actor-Critic methods
7. State Representation
   - Value Function Approximation
   - Stochastic Gradient Descent
8. Basics of Neural Networks (review or refer to ECE657A content)
   - fully connected, multi-layer perceptrons
   - supervised training, back-propagation
   - regularization methods
9. Deep Reinforcement Learning
   - Deep Q- Networks (DQN)
   - Experience replay buffers and mini-batch training
   - A2C, DDPG, PPO
1. Other Challenges (brief)
   - Partially Observable MDPs (POMDPs)
   - Multi-Agent RL (MARL)
1. Other ways to solve (PO)MDPs (if time permits)
   - Monte-Carlo Tree Search, Explaining AlphaGo
   - Curiosity based learning
   - Soft-Actor Critic
1. Wrap-up and Review

## Getting Help:

- **Discussion board:** 
  - *Piazza* will be the main place for detailed discussion and questions. Students can post anonymously (from students only), post a collaborative answer and course staff can confirm these, post their own or run Live Q&A events.
  - Go there there and sign up with your UWaterloo email now!
- **Pre-recorded Video Lectures:** These will be made available on the [course youtube channel](https://www.youtube.com/channel/UC7vU2kP8oNwvr0GuAqoxYGA), and links from within Learn
- **LEARN Website:** The main course content, announcements, grade tracking and materials will be made available on Learn. All registered students should see this in their LEARN courses.
- **Email the Teaching Assistant and Instructor:** Office Hours will be arranged once term starts as needed.
- **AccessAbility Services :** http://uwaterloo.ca/accessability-services 
  - If you need any accommodation, assistance with exams, learning environment, assignments, talk to this office and they can help you set it up as securely and anonymously as possible.

### Discussion Group Protocols

- Posts on Piazza can be public or anonymous to your classmates, but they will *never* be anonymous to the TAs and Instructor. 
- Be kind. Assume the best, not the worst. Think before you hit enter.
- Posts which are considered offensive, abusive, bullying, discriminatory to any group or person, will be made private or deleted and followed up with private discussion.
- If you feel there is inappropriate, hurtful behaviour occurring on the discussion forum, please notify the professor, TAs or department staff as you feel appropriate. 
- If you really can't get in touch with anyone and it is an emergency you can contact Prof. Crowley directory via Microsoft Teams messaging (please don't abuse this though :| )

## Course Resources

### Primary Reference for Course

**[SuttonBarto2018]** - Reinforcement Learning: An Introduction. Book, free pdf of draft available.
http://incompleteideas.net/book/the-book-2nd.html

### Other Useful Texts

**[Dimitrakakis2019]** - Decision Making Under Uncertainty and Reinforcement Learning

http://www.cse.chalmers.se/~chrdimi/downloads/book.pdf

**[Ghavamzadeh2016]** - Bayesian Reinforcement Learning: A Survey. Ghavamzadeh et al. 2016.
https://arxiv.org/abs/1609.04436

- More probability notes online: https://compthinking.github.io/RLCourseNotes/

### Open AI Reference Website

This website is a great resource. It lays out concepts from start to finish. Once you get through the first half of our course, many of the concepts on this site will be familiar to you.

- Key Papers in Deep RL List - https://spinningup.openai.com/en/latest/spinningup/keypapers.html

- Fundamental RL Concepts Overview - The fundamentals of RL are briefly covered here. We will go into all this and more in detail in our course.
  https://spinningup.openai.com/en/latest/spinningup/rl_intro.html

 - Family Tree of Algorithms - Here, a list of algorithms at the cutting edge of RL as of 1 year ago to so, so it's a good place to find out more. But in a fast growing field, it may be a bit out of date about the latest now.
https://spinningup.openai.com/en/latest/spinningup/rl_intro2.html



General University of Waterloo Guidelines:
------------------------------------------

**Academic Integrity:** In order to maintain a culture of academic
integrity, members of the University of Waterloo community are expected
to promote honesty, trust, fairness, respect and responsibility. Check
http://www.uwaterloo.ca/academicintegrity/ for more information.

**Grievance:** A student who believes that a decision affecting some
aspect of his/her university life has been unfair or unreasonable may
have grounds for initiating a grievance. Read Policy 70, Student
Petitions and Grievances, Section 4,
http://www.adm.uwaterloo.ca/infosec/ Policies/policy70.htm. When in
doubt please be certain to contact the departments administrative
assistant who will provide further assistance.

**Discipline:** A student is expected to know what constitutes academic
integrity---check http: //www.uwaterloo.ca/academicintegrity/ to avoid
committing an academic offence, and to take responsibility for his/her
actions. A student who is unsure whether an action constitutes an
offence, or who needs help in learning how to avoid offences (e.g.,
plagiarism, cheating) or about rules for group work/collaboration should
seek guidance from the course instructor, academic advisor, or the
undergraduate Associate Dean. For information on categories of offences
and types of penalties, students should refer to Policy 71, Student
Discipline, http://www.adm.uwaterloo.ca/infosec/Policies/policy71.htm.
For typical penalties check Guidelines for the Assessment of Penalties,
http://www.adm.uwaterloo.ca/infosec/guidelines/penaltyguidelines.htm.

**Appeals:** A decision made or penalty imposed under Policy 70 (Student
Petitions and Grievances) (other than a petition) or Policy 71 (Student
Discipline) may be appealed if there is a ground. A student who believes
he/she has a ground for an appeal should refer to Policy 72 (Student
Appeals) http://www.adm.uwaterloo.ca/infosec/Policies/policy72.htm.

**Note for Students with Disabilities:** The Office for Persons with
Disabilities (OPD), located in Needles Hall, Room 1132, collaborates
with all academic departments to arrange appropriate accommodations for
students with disabilities without compromising the academic integrity
of the curriculum. If you require academic accommodations to lessen the
impact of your disability, please register with the OPD at the beginning
of each academic term.
