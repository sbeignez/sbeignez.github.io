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

> __Independence of 2 events__: Event A and B are independent if knowing 1 occured, it does not change the probability of the other:
> $$ P(A | B) = P(A) or P(B | A) = P(B)$$
> (when $P(B) \ne 0$ or P(A))  
> or:  
> $$ P(A \cap B) = P(A)P(B) $$

* Disjoint events are NOT independants.  
* Independence is about information.  
* Events are independent when (for example) they are caused by 2 distinct and non-interacting physical processes.

* Two disjoint events are never independant.
* $A$ and $A^c$ are not independents (excepts if P(A) =0 or 1)
* $A$ and $\bar{A}$ are independent only if $P(A) = 0$ or $1$.

* __Independence of complements__: If A et B are independent, then A and B', A' and B, A' and B'.

### `01.5.2` Conditional independence
> __Conditional independence__:
> $$ P(A \cap B | C) = P(A |C)*P(B|C) $$
> Then A and B are conditionally independent on C  
> (when $P(C) \ne 0$)

* Independent does not imply conditional independence, and vice versa.

### `01.5.3` Independence of a collection

> __Independence of a collection__  
> $A_a, A2, ..A_n$ are independent if:
> $$ P(\bigcap_i A_i) = \prod_i P(A_i)$$
> for every subsets S of {1,2,..., n}

> __Pair-wise independence__:

* Pair-wise independence does not imply independence!
* $ P(A \cap B \cap C) = P(A)*P(B)*P(C)$ do not imply independence of the collection $A, B, C$.
* $P(\bigcap_i A_i) = \prod_i P(A_i)$ do not imply independence of the collection $A_i$

### `01.5.4` Application: __Reliability__ problems

For calculating the reliability of a system of connected elements. Each elements has a probablity $p$ to be up and $1-p$ to fails. Each elements are independent.
* elements in serie: $ p_1 * p_2 $
* elements in parallele: $ 1 - (1-p_1)(1-p_2) $



