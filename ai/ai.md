---
title: A.I.
---

# Definition

> __Articifial Intelligence__: Study and construction of rational agents.

> __Rational agent__: An agent that acts so as to acheive the best outcome, according an objective.  
> (or under uncertainty, the best expected outcome). Effective behaviour. 


> __Machine Learning__: Branch of A.I. and C.S. that create agents, that can act rationally in ciscumstances that are new. Adapt to new situations.

> __Supervised Learning__: make prediction from data. (it's not actual plannig or acting toward an objective)

* Can a machine learn from an algorithm? = Supervised learning  

> __Reinforcement Learning__: Learn from experience of new situation? Exploration.

> __Neural Network__: A NN is an approximation function of an target function f, which parameters, the weights and biases, are pre-calculated | instanciated using a large number of "labelled" data (observed inputs and output of the taget function), using the gradient descent algorithm.
> The technic works even though the labelled data can potentially contains some noise.

> __Operation Research__:

> __Algorithm__:

> __Control theory__:

> __Game therory__:



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
