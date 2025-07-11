---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

This is Zhouyu Zhang's (章舟宇) website. Every thing is still under construction, myself as well. I am advised by Dr. [Yue Chen](https://sites.google.com/view/bm2lab), then Dr. [Glen Chou](https://glenchou.github.io/).

Research Interest
------
I like **optimization**. 

> "People optimize. "
> — Jorge Nocedal, *Numerical Optimzation*

Optimization is something that structurally solves complicated problems, in both forward way and inverse way. In the forward sense, the ones who make decisions base their strategy upon certain goals and subject themselves to must-obey constraints, thus producing solutions (e.g. configuration space shapes, control policies ...) that they can at least tell local optimium. For example, a robotic arm planning reaching objectives while respecting actuation constraints (the motors will actually explode if not properly powered). In the inverse sense, the execution of the policies are observed, and goals & constraints of the demonstrator are speculated. We can think of this as a diligent apprentice that observes a master's pro moves and tries to guess what is the driving motive.

Both the forward & inverse viewpoints find their application well in the robotics domain, which I conduct research on. I apply optimization-based ideas to various settings of robots, either through forward optimal solution generation, or inverse objective/constraint inference from demonstrations.

Robotic Applications
------
For continuum robots, solving the kinematics poses a significant challenge, due to the high nonlinearity in the actuation to task space mapping, and the compliant & soft nature of the robot body. Solution of continuum robot kinematics in **free space** often times require shooting methods, which suffers from numerical instability and inability to handle hard constraints. In [this work](https://arxiv.org/pdf/2308.10770), we explored methods that can compute continuum robot kinematics in **constrained space**, by formulating the task into an optimization problem with quadratic costs and nonlinear constraints. We also leveraged local linearity of actuation to task space mapping to provide stable initial guesses.

For robots that have simpler dynamics but greater decision space, like the scenario in multi-agent systems, inverse inference of goals & constraints are usually as important as generating optimal control policies, as the latter will require some level of knowledge of the former. You do not want to miscalculate other robots' intentions and proximity tolerance, otherwise we will have a scary (or cute) car crash. In [this work](https://iscicra25.github.io/papers/2025-Zhang-15_Constraint_Learning_in_Mult.pdf), we studied how one can formally infer the hard constraints that are well-respected by others in the multi-agent systems, from locally optimal trajectories demonstrated. Through the lens of game theory and inverse optimal control, the hard constraints can be exactly recovered.

Some clouds of underexploration still loom, though.
------
1. Many optimization problem suffers from curse of dimension. In the inverse case of multi-agent systems, the joint decision space can get crazily large when we have too many agents or high dimension dynamics, thus becoming computationally prohibitive. How can we effectively compress the state space, without sacrificing too much of the objective/constraints inference quality?
2. How should we formulate the inverse problem, if the demonstrations/observations come in degraded quality? The experts are not perfect, they undergo disturbances during their tutorial footage. But they made adjustments quick so that the demostrations are still very optimal. Can the apprentice be a smart learner?
3. Can we apply the objective/constraint inference structure to policies gained from reinforce learning? In some settings, like an atari game, the objective can not be formally or explicitly expressed in optimization language, but RL algorithms excels at finding a winning strategy for those games. I hope the inverse structure can work as lens that explain the RL policy, by answering questions like "At time t, why did you do action a_t given state s_t?"
4. Inverse & forward constrained reinforcement learning. I came across the series of papers a week ago, haven't read yet. But I list some questions here, hoping I can answer in the near future. How are the constraints incorporated into the problem? Is it a soft way (like setting a steep coefficient for the constraint violation in the cost), or a hard way (some other methods that explicitly ensures constraint satisfaction)?
5. Constraints work closely with safety. If a robot does not violate constraints then it is safe. Safety is a real concern for robots that work closely with delicate objects, like a human. Learning based methods excel in generalizability, which means they do not need meticulous mathematical struturing of the envrionment to generate a decent policy, but often fail to answer safety related concerns due to their probability based nature. How can we regulate learning based methods, via optimziation language and mindsets? Does the regulation come as a natural component in the learning based algorithm, or as a post-filter of the actions/policies generated? Many questions need to be answered. 