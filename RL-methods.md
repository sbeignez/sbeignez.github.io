---
title: RL methods
description: RL methods
tags: RL
latex: false
---

# Model-based RL

### Policy 
\\ \pi(s) =    
$\pi*$: Optimum policy 

### Quality function
Quality of a state-action pair
$$ Q(s,a) = \sum_{s'\in S}( P(s'|s,a) * ( R(s,a,s') + \gamma * V(s') ) )$$

### Value function
\\ V(s) = max_a Q(s,a) \\


# Model-free RL
When P and R are unknown

## Monte Carlo Learning

Total cumulative reward:
$$ R = \sum_{k=1}^n \gamma^k r_k $$

Episodic .. algo: total reward over episode  
With definitive end

Update:

$$ V(s_k) \larr V(s_k) + {1 \over n} ( R_{\sum} - V(s_k)), for all k \in [1,...,n]$$

## Temporal Difference Learning: TD(N)

$$ V(s_k) = E(r_k + \gamma V(s_{k+1})) = E(r_k + r_{k+1} \gamma V(s_{k+2})) $$

$$ V(s_k) \larr V(s_k) + \alpha ( r_k + \gamma V(s_{k+1}) - V(s_k))$$


## Q-Learning

Off-policy TD(0) learning: can take random (sub-optimal) actions

## SARSA

On-policy: for $a_{k+1}$
