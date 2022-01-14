---
title: Latex with GitHub Pages
---

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.css" integrity="sha384-yFRtMMDnQtDRO8rLpMIKrtPCD5jdktao2TV19YiZYWMDkUR5GQZR/NOVTdquEx1j" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/katex.min.js" integrity="sha384-9Nhn55MVVN0/4OFx7EE5kpFBPsEMZxKTCnA+4fqDmg12eCTqGi6+BB2LjY8brQxJ" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.10.2/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>

# Model-based RL

### Policy 
$\pi(s) =  $  
$\pi*$: Optimum policy 

### Quality function
Quality of a state-action pair
$$ Q(s,a) = \sum_{s'\in S}( P(s'|s,a) * ( R(s,a,s') + \gamma * V(s') ) )$$

### Value function
$ V(s) = max_a Q(s,a)$





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

$ V(s_k) = E(r_k + \gamma V(s_{k+1})) = E(r_k + r_{k+1} \gamma V(s_{k+2})) $

$$ V(s_k) \larr V(s_k) + \alpha ( r_k + \gamma V(s_{k+1}) - V(s_k))$$


## Q-Learning

Off-policy TD(0) learning: can take random (sub-optimal) actions

## SARSA

On-policy: for $a_{k+1}$

---
* https://stackoverflow.com/questions/26275645/how-to-support-latex-in-github-pages
* https://kevinfossez.github.io/posts/2020/04/blog-post-1/