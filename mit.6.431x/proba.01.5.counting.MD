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

## `01.6.2` Permutations

Number of ways of ordering n elements (from an un-ordered set, into slots)  
Repetition is prohibited

> Number of permutations, of $n$ elements: $n!$

## `01.6.3` Number of subsets
> Number of subsets of $\{1...n\}$: $2^n$  

Subsets includes the whole set and the empty set.

## `01.6.4` Combination

From a set of $n$-elements, build a sub-set of $k$-elements.
> $$ {n \choose k} =  $$  
> 

Construct an __ordered__ sequence of $k$ __distinct__ items
1. Directly
    * $ { n! \over (n-k)! } $
2. Step a and b  
    * a. $ \binom{n}{k} $   
    * b. 

## `01.6.` Partitions
The binomial probability


PRoblem solving
- assume all outcomes are

| From | To | Formula
| --- | --- | ---
| Set (Non-Ordered, Non-Repeat) $n$ | Permutation (Ordered, Non-Repeat) | $n!$
| Set (Non-Ordered, Non-Repeat) $n$ | Sub-Set (Non-Ordered, Non-Repeat) | $2^n$
| Set (Non-Ordered, Non-Repeat) $n$ | $k$ Permutation (Ordered, Non-Repeat) | ${ n! \over (n-k)! }$
| Set (Non-Ordered, Non-Repeat) $n$ | $k$ Permutation (Ordered, Non-Repeat) | ${ n! \over (n-k)! }$
| Ordered | To non-ordered | $ 1 / n! $
