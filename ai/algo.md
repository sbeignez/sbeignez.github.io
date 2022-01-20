# Algo

## Divide and Conquer

Divide > Solve > Combine

```
Input: p, a problem of type <P>
Output: a, an answer of type <A>
Begin Algorithm

DC(p <P>):
    [recursion]
    if
        the problem is solvable isSolvable(p)
            (eg. size(p) is small enough).
    then
        return Solve(p).
    else
    [divide & conquer & combine]
        *divide*: Divide the problem p into k sub-problems p1, ..., p_k,
            such as Union(p_i)=p and Inter(p_i,p_j)=0 (MECE, Mutually Exclusive and Commonly Exhaustive).
        *conquer*: solve each sub-problem, by applying DC() to each p_i. Or continue to divide recursively.  
        *combine* Combine(DC(p1), DC(p2), ..., DC(p_k)) --> answer.
        return answer.

isSolvable(<P>) -> <Bool>
Solve(<P>) -> <A>
Divide(<P>) -> List<P>
Combine(list<A>) -> <A>
```
Note: a recursive problem can always be written using iterative approach and vice versa

#### D&C examples
* Sorting: mergesort and quicksort
* Counting inversions
* Closest-pair algo
* Tree traversals
* Binary search
* Multiplication of large integers
* Matrix multiplication: Strassen’s algorithm
* Closest-pair and convex-hull algorithms

## Dynamic Programming

Overlapping sub-problems
Solutions stored in table: memorization-memoization or tabulation
* Memoization (top-down cache filling)
* Tabulation (bottom-up cache filling)


## VS.

### Divide and Conquer vs. Dynamic Programming

D&Q | DP
--- | ---
divide the problem, recursively breaking down the problem | .
sub-problems are independant (non-overlapping) | sub-problems overlap (re-use subtree solutions)
(non-)recursive? | recursive
combines the solutions of the subproblems to obtain the solution of the main problem | uses the result of the subproblems to find the optimum solution of the main problem.


# Recursion

## Recursion to iteration
How to 
