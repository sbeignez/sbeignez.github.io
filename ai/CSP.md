# CSP Contrains Satisfaction Problems

AIMA.Chapter 5.
En:CSP = Fr:Programmation par contraintes

CSP problem exmaples
* cryptarithmetic
* N-queens
* map coloring


Categories:
* Constraint Satisfaction Problems (CSP)
    * Constrained Optimization Problems (COP), with preference constraints
        * Linear Programs


Algo:

* AC-3
* PC-2

Backtracking search
## Speed-ups

## Speed-up 1. Ordering

## Speed-up 2. Filtering
Forward Checking

### Filtering 1: Arc consistency
Consistency: do not violate a constraints
1-consistency (node)
2-consistency (arc): Pair of nodes
K-consistency: (1,..,K-1) -> K

Strong n-consistency


## Speed-up 3. Structure

Contraints graph
- indenpendant sub-problems
- Tree strucutre graph (acyclic)

Ordering of the tree
Remove Backward Arc consistency
Assign forward


## Cutset conditioning


## Tree Decomposition
- mega variables

## Iterative Improvement

Min-conflicts algo
Choose conflicted varaible
Pick the least

Performance:
Solve in constrant time
R = number_of_constraints/ number_of_variables
excpt. range ratio R in [.,.]



## Local Search
Simulated Annealing

## Genetic Algorithms


---
Cours:
* https://perso.liris.cnrs.fr/christine.solnon/Site-PPC/e-miage-ppc-som.htm