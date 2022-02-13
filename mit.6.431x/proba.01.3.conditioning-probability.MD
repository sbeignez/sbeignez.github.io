# Probability. Chapter 01. Sample Space and Probability

# `01.` Sample Space and Probability

## `01.3.` Conditioning Probability [Lecture 2]

Revising a model based on new information
Divide-and-conquer tools

Tools:
* Multiplication rule
* Total probability theorm
* Bayes's rules (inference)


#### `01.3.1` The Conditional probability definition

> __Conditional probability__  
> When B uniform distribution?? 
> $$ P(A|B) = { P(A \cap B) \over P(B) }$$
 
CP obeys to same axioms:
* $ P(A|B) <= 1 $
* $ P( \Omega | B ) = 1 $
* $ P( B | B ) = 1 $
* Additivity: If A,B disjoints: $ P( A \cup B | C ) = P( A | C ) + P( B | C ) $


Use of CP:
* 1/ Revise a model, with new information
* 2/ Build a multi-stage model of a probabilistic experiment

#### Example: the radar


#### `01.3.2` The multiplication rule

> The __multiplication rule__
> $$ P( E_1 \cap E_2 ) = P(E_1) * P(E_2 | E_1) $$ 
> $$ P( \bigcap_{k=1}^n E_k) = P(E_1) * \prod_{k=2}^n P(E_{k} | \bigcap_{j=1}^{k-1} E_{j}) $$

#### `01.3.3` The total probability theorem

> The __total probability theorem__
> $$ P(B) = \sum P(A_i)P(B|A_i)$$

Partition of $\Omega$, $A_1, A_2, .. A_n$  
Weighted average of $P(B|A_i)$

## `01.4.` Bayes's rule

> The __Bayes'rule__
> $$ P(A_i | B) = { P(A_i)*P(B | A_i) \over \sum_j P(A_j)* P(B|A_j) } $$

Bayesian inference

$$ A_i  \xRightarrow[ P(B|A_i)  ]{ model    }  B    $$
$$ B    \xRightarrow[ inference ]{ P(B|A_i) }  A_i  $$


## `01.5.` Independence [Lecture 3]

> __Independence of 2 events__: Event A and B are independent is: 

> __Conditional independence__:

> __Independence of a collection__

> __Pair-wise independence__:

> __Reliability__:

Unrelated source of randomness

