---
title: 'Unanswered questions ahead'
date: 2025-07-15
permalink: /posts/2025/07/unanswered_questions/
tags:
  - questions
  - research
---

Challenges Ahead
======
1. Many optimization problem suffers from curse of dimension. In the inverse case of multi-agent systems, the joint decision space can get crazily large when we have too many agents or high dimension dynamics, thus becoming computationally prohibitive. How can we effectively compress the state space, without sacrificing too much of the objective/constraints inference quality?

2. How should we formulate the inverse problem, if the demonstrations/observations come in degraded quality? The experts are not perfect, they undergo disturbances during their tutorial footage. But they made adjustments quick so that the demostrations are still very optimal. Can the apprentice be a smart & robust learner?

3. Can we apply the objective/constraint inference structure to policies gained from reinforce learning? In some settings, like an atari game, the objective can not be formally or explicitly expressed in optimization language, but RL algorithms excels at finding a winning strategy for those games. I hope the inverse structure can work as lens that explain the RL policy, by answering questions like "At time t, why did you do action a_t given state s_t?"

4. Inverse & forward constrained reinforcement learning. I came across the series of papers a week ago, haven't read yet. But I list some questions here, hoping I can answer in the near future. How are the constraints incorporated into the problem? Is it a soft way (like setting a steep coefficient for the constraint violation in the cost), or a hard way (some other methods that explicitly ensures constraint satisfaction)?

5. Constraints work closely with safety. If a robot does not violate constraints then it is safe. Safety is a real concern for robots that work closely with delicate objects, like a human. Learning based methods excel in generalizability, which means they do not need meticulous mathematical struturing of the envrionment to generate a decent policy, but often fail to answer safety related concerns due to their probability based nature. How can we regulate learning based methods, via optimziation language and mindsets? Does the regulation come as a natural component in the learning based algorithm, or as a post-filter of the actions/policies generated? Many questions need to be answered. 

------