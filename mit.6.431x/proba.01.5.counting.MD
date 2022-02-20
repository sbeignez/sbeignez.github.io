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
> Number of subsets of $\{1...n\}$: $2^n$  

Subsets includes the whole set and the empty set.

Note: It's the sum of all k-sub-sets (k-combinations) over $0 \le k \le n$.


## `01.6.3a` Permutations

Number of ways of ordering n elements (from an un-ordered set, into slots)  
Repetition is prohibited

> Number of permutations, of $n$ elements:
> $$ n! $$

## `01.6.3b` k-Permutations

Number of ways of ordering k elements, out of a set of n elements.

> $$ {n! \over (n-k)!} $$ 

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

## `01.6.5` Partitions

> $$ \sum_{k=0}^n \binom{n}{k} = \binom{n}{0} + \binom{n}{1} + ... + \binom{n}{n} = \binom{n}{0, 1, ..., n} = 2^n $$


## `01.6.5` The binomial probability

Proof:  
$ P(\text{a particular k head sequence}) = p^k (1-p)^{n-k} $  
$ P(\text{k head}) = p^k (1-p)^{n-k} \cdot \binom{n}{k} $

> Binomial coefficients
> $$ \binom{n}{k} \cdot p^k \cdot (1-p)^{n-k}$$

Note: The sum over all size sub-sets, $ \sum_{k=0}^n \binom{n}{k} \cdot p^k \cdot (1-p)^{n-k} $, is of course $= 1$.

PRoblem solving
- assume all outcomes are

| From | To | Formula
| --- | --- | ---
| Set (Non-Ordered, Non-Repeat) $n$ | Permutation (Ordered, Non-Repeat) | $n!$
| Set (Non-Ordered, Non-Repeat) $n$ | Sub-Set (Non-Ordered, Non-Repeat) | $2^n$
| Set (Non-Ordered, Non-Repeat) $n$ | $k$ Permutation (Ordered, Non-Repeat) | ${ n! \over (n-k)! }$
| Set (Non-Ordered, Non-Repeat) $n$ | $k$ Permutation (Ordered, Non-Repeat) | ${ n! \over (n-k)! }$
| Ordered | To non-ordered | $ 1 / n! $



