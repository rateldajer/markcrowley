---
layout: post
date: 2021-11-01 16:41:00-0400
inline: false
title: Patent awarded for Multi-level collaborative vehicle control
description: Patent arose in collaboration with DENSO Inc. on a remote controlled car demo for CES.
meta: patent
topics: reinforcement-learning 
domains: autonomous-driving
people: sriramganpathisubramanian, sushrutbhalla, japsreetsambee, sebastianfischmeister, markcrowley 
showdomains: true
showpeople: false
showtags: false
showmethods: false
showbib: false
img: /assets/img/patent-design.png
publish: true
---

We recently had a patent fully approved and published on a method for multi-level collaborative control of vehicles using control and reinforcement learning working in tandem. The work resulted from a demonstration we created with Denso International for the 2018 CES technology show. 

<a href="/assets/img/patent-design.png" border=0><img src="/assets/img/patent-design.png" align=right width=300></a>
- **Patent Number**:
- **Title**: Multi-level collaborative control system with dual neural network planning for autonomous vehicle control in a noisy environment
- **Inventors** (members of my lab in bold): Zhiyuan DU, Joseph Lull, Rajesh MALHAN, **Sriram Subramanian**, **Sushrut BHALLA**, **Jaspreet SAMBEE**, **Mark Crowley**, Sebastian Fischmeister, Donghyun Shin, William Melek, Baris Fidan, Ami Woo, Bismaya Sahoo
- **Link**: https://patents.google.com/patent/US11131992B2/en 


> A RLP system for a host vehicle includes a memory and levels. The memory stores a RLP algorithm, which is a multi-agent collaborative DQN with PER algorithm. A first level includes a data processing module that provides sensor data, object location data, and state information of the host vehicle and other vehicles. A second level includes a coordinate location module that, based on the sensor data, the object location data, the state information, and a refined policy provided by the third level, generates an updated policy and a set of future coordinate locations implemented via the first level. A third level includes evaluation and target neural networks and a processor that executes instructions of the RLP algorithm for collaborative action planning between the host and other vehicles based on outputs of the evaluation and target networks and to generate the refined policy based on reward values associated with events.
