---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

This is Zhouyu Zhang's (章舟宇) website. Every thing is still under construction, myself as well. After obtaining my Bachelor's Degree from Tsinghua University, Beijing, I now pursue my PhD in Robotics at Georgia Intitute of Technology. I am advised by Dr. [Yue Chen](https://sites.google.com/view/bm2lab), then Dr. [Glen Chou](https://glenchou.github.io/).

Research Interest
------
I work on **optimization**.

> "People optimize. "
> — Jorge Nocedal, *Numerical Optimzation*

Optimization provides a structural lens for solving complicated problems, both in the forward and inverse sense. Forward optimization is what you’d expect: decision-makers define objectives, accept some non-negotiable constraints, and produce strategies accordingly — for instance, shaping configuration spaces or generating control policies (hopefully not ones that make your robot explode). In the inverse sense, we observe the resulting behavior and reverse-engineer the likely goals and constraints — much like a diligent apprentice watching a master at work and trying to infer their intentions.

These two perspectives converge elegantly in robotics. My research leverages both: I use optimization not only to generate optimal behavior but also to recover the structural principles that govern it.

Robotic Applications
------
In the world of continuum robots, kinematics isn’t just hard — it’s soft, in all the worst ways. The actuation-to-task-space mapping is highly nonlinear, and the robots themselves are compliant, squishy entities that defy intuition. Solving their motion in free space often requires shooting methods, which are famously unstable and allergic to hard constraints. In [this work](https://arxiv.org/pdf/2308.10770), we proposed a more grounded approach: recasting kinematics as a constrained optimization problem with quadratic costs and nonlinear constraints. By exploiting local linearity in the actuation-to-task-space mapping, we generate reliable initial guesses and stable solutions.

![Constrained Kinematics](/images/CTR_paper_figure.png)

<!-- For robots that have simpler dynamics but greater decision space, like the scenario in multi-agent systems, inverse inference of goals & constraints are usually as important as generating optimal control policies, as the latter will require some level of knowledge of the former. You do not want to miscalculate other robots' intentions and proximity tolerance, otherwise we will have a scary (or cute) car crash. In [this work](https://iscicra25.github.io/papers/2025-Zhang-15_Constraint_Learning_in_Mult.pdf), we studied how one can formally infer the hard constraints that are well-respected by others in the multi-agent systems, from locally optimal trajectories demonstrated. Through the lens of game theory and inverse optimal control, the hard constraints can be exactly recovered. -->

Meanwhile, robots with simpler dynamics but more complex decision-making, like those in multi-agent systems, introduce a new challenge: inference. It’s not enough to compute optimal strategies — you must also deduce what others are optimizing for. Misjudging another robot’s goals or proximity tolerance might lead to a dangerous (or, depending on your mood, adorable) fender-bender. In [this work](https://iscicra25.github.io/papers/2025-Zhang-15_Constraint_Learning_in_Mult.pdf), we formalized the inverse problem: learning the hard constraints respected by other agents, based on their locally optimal trajectories. Using tools from game theory and inverse optimal control, we showed that these constraints can, in fact, be exactly recovered.

<!-- Nevertheless, many questions lie answered in front of my path. Check this [post](/posts/2025/07/unanswered_questions/) for the thinking I am current having. -->

Many questions remain unanswered — structurally, philosophically, and computationally. You can find a collection of such questions [here]({{ site.baseurl }}/posts/2025/07/unanswered_questions/). They keep me up at night.