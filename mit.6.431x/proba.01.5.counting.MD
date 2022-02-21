# Probability. Chapter 01. Sample Space and Probability

# `01.` Sample Space and Probability

## `01.6.` Counting `[Lecture 4]`

The field of combinatorics:
* Enumeration (Counting) - arrangements or configurations

## `01.6.1` The counting principle
 
> $r$: number of stages  
> $n_i$: number of choices at stage $i$  
> Number of choices = $n_1 * n_2 * .. n_r$

sequence process to construct the solution  
each step is independent from the other ones.  
Or when Repetition is allowed

## `01.6.2` Number of subsets
> Number of subsets of $\{1...n\}
> $$ = 2^n $$  

Subsets includes the whole set and the empty set.

Note: It's the sum of all k-sub-sets (k-combinations) over $0 \le k \le n$.


## `01.6.3a` Permutations

Number of ways of ordering n elements (from an un-ordered set, into slots)  
Repetition is prohibited

> Number of permutations, of $n$ elements:
> $$ = n! $$

## `01.6.3b` k-Permutations

Number of ways of ordering k elements, out of a set of n elements.

> $$ = {n! \over (n-k)!} $$ 

## `01.6.4` Combination

From a set of $n$-elements, build a sub-set of $k$-elements.
> $$ {n \choose k} =  {n! \over k!(n-k)!} $$  
> Say: "$n$ choose $k$"

Proof: Construct an __ordered__ sequence of $k$ __distinct__ items, from 2 ways:
1. Directly
    * $ { n! \over (n-k)! } $
2. Step a and b  
    * a. $ \binom{n}{k} $   
    * b. k!

Some combinations results:

> $ \binom{n}{n} = {n! \over n!(n-n)!}= 1 $, 

> $ \binom{n}{0} = {n! \over 0!(n-0)!}= 1 $, which is $\empty$.

> $$ \sum_{k=0}^n \binom{n}{k} = \binom{n}{0} + \binom{n}{1} + ... + \binom{n}{n} = \binom{n}{0, 1, ..., n} = 2^n $$

## `01.6.5` Partitions

$n$ elements set ($n \ge 1$)  
Split in $r$ groups.  
$ n_1 + n_2 + n_3 + ... + n_r = n $ (all n_i are non-negative)

> number of partitions = 
> $$ = \binom{n}{n_1} \binom{n - n_1}{n_2} \binom{n - n_1 - n_2}{n_3} \cdot ... \cdot  \binom{n - n_1 - n_2 - ... - n_{r-1}}{n_r} $$
> $$ = {n! \over n_1! \cdot n_2! \cdot ... \cdot n_r! }$$




## `01.6.5` The binomial probability

Proof:  
$ P(\text{a particular k head sequence}) = p^k (1-p)^{n-k} $  
$ P(\text{k head}) = p^k (1-p)^{n-k} \cdot \binom{n}{k} $

> Binomial coefficients
> $$ \binom{n}{k} \cdot p^k \cdot (1-p)^{n-k}$$

Note: The sum over all size sub-sets, $ \sum_{k=0}^n \binom{n}{k} \cdot p^k \cdot (1-p)^{n-k} $, is of course $= 1$.



| Transformation | From | To | Formula
| --- | --- | --- | ---
| __Permutation__<br> Unordered $\to$ Ordered | __Set__<br>- Non-Ordered<br>- Non-Repeat | __List__<br> - Ordered | $$ n! $$ 
| Ordered $\to$ Un-Ordered | All Lists | a Set | $$ * {1 \over n!} $$
| __k-Permutation__<br>Unordered $\to$ Ordered<br>Pick $k$-elements out of $n$<br>  | Set (Non-Ordered, Non-Repeat) $n$ | __List__<br> $k$ Permutation (Ordered, Non-Repeat) | $${ n! \over (n-k)! }$$
| __Combinations__<br>Unordered<br>Pick $k$-elements out of $n$<br> | Set of $n$-elements | Sub-Sets of $k$-elements | $${ n! \over k! (n-k)! }$$
| __Set $\to$ all Sub-sets__<br>  | __Set__<br>- Non-Ordered<br>- Non-Repeat | __Sub-Set__ of all sizes $k$-elements, from 1 to n | $$2^n$$




### Probablity problem solving
- assume all outcomes are
- Solve sequentially: Constructing configuraion step by steps. steps must be (independents?)
- Process in stages
- counting principle
- Building a tree
- same number of options at each stages (whatever the choice at previous stage). can't be different.
