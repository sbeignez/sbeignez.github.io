---
title: A.I.
---

# Artificial Intelligence

linguistics, bias, vision, planning, robotic process automation, natural language processing, decision science, etc
machine learning
neural network
robotics
expert systems
fuzzy logic
natural language processing



##  Artificial Intelligence

* Problem-Solving
    * [Problem-solving by Search](/ai/algo)
    * [Adversarial search] and [Games Theory](/ai/game-theory)
    * [Contraints Satisfaction Problems](/ai/csp)
        * Linear Programming
    * Evolutionary methods  
        *Genetics Algorithms, Genetic Programming, NEAT*
* Machine Learning
    * Unsupervised Learning
    * Supervised Learning
    * Deep Learning
    * [Reinforcement Learning](/ai/RL)


## Reinforcement Learning

* Tabular Solutions Methods
    * Finite Markov Decision Process (MDP)
    * Dynamic Programming
    * Monte Carlo Methods
    * Temporal-Difference Learning  
* Approximate Solutions Methods
    * On-policy
    * Off-policy


## Types of problems

CSP | Search | Game | RL
--- | --- | --- | --- 
1 state, multiple variables | Multiple states | = | =
. | Actions | = | = 
. | Graph of states and actions | Graph of states and actions, with utilities | MDP Markov Decision Process, with Probabilistic Transitions and Rewards 
. | 1 initial state | = | = 
. | 1 goal state | multiple terminal states | =
. | 1 agent | Multi-agents adversaries | stochastic env
. | transitions are deterministic | transitions are deterministic, but other agents and chance nodes not | transitions are stochastic
. | Value(state) | Utility(state) | Q Value(state)
. | Optimize path cost | Optimize outcome | Optimize Expected Reward 
