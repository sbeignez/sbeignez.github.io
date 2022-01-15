# Algo

## Divide and Conquer

Divide > Solve > Combine

input: problem of size n P_n

```
Algorithm DC(P: problem):
    [recursion]
    if
        the P is solvable (eg. size(P) is small enough).
    then
        return Solve(P).
    else
    [divide & conquer & combine]
        *divide*: Divide the problem P into k sub-problems P1, ..., Pk,
            such as Union(Pi)=P and Inter(Pi,Pj)=0 (MECE, Mutually Exclusive and Commonly Exhaustive).
        *conquer*: solve each sub-problem, by applying DC() to each Pi. Or continue to divide recursively.  
        *combine* Combine(DC(P1), DC(P2), ..., DC(Pk)) --> answer.
        return answer.
```


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
sub-problems are independant | sub-problems overlap
recursive | non-recursive ?
combines the solutions of the subproblems to obtain the solution of the main problem | uses the result of the subproblems to find the optimum solution of the main problem.