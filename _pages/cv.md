---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Robotics, Georgia Institute of Technology, 2022 - 2028 (expected)
* M.S. in Electrical and Computer Engineering, Georgia Institute of Technology, 2023 - 2025
* B.S. in Engineering Physics, Tsinghua University, 2018 - 2022

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>


Experience
======
* Summer 2025: [Virtual Summer Internship Program (VSIP)](https://ospo.cc.gatech.edu/vsip/) 
  * [Georgia Tech Open Source Program Office](https://ospo.cc.gatech.edu/)
  * Duties includes: Contribute to the [GTSAM](https://github.com/borglab/gtsam) open-source SLAM repository
  * Supervisor: Dr. [Frank Dellart](https://dellaert.github.io/)
  
Skills
======
* Programming Language: C/C++, Python, Matlab, 
* Robotics: ROS2, Linux, Pytorch, PyBullet
* Optimization Tools: CasADi, Gurobi, cvxpy
* Optimization Techniques: Nonlinear Programming (NLP), Mixed Integer Programming (MIP)


  
<!-- Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul> -->
  
<!-- Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul> -->
  
Service and leadership
======
* Reviewer for RA-L, IROS, CoRL
