# 5. CSP Contraints Satisfaction Problems [AIMA]

- `05` Contraints Satisfaction Problems 
    * `05.1` Defining Contrains Satisfaction Problems
    * `05.2` Constraint Propagation: Inference
    * `05.3` Backtracking Search for CSP
    * `05.4` Local Search for CSP
    * `05.5` The Structure of problems

---

Fr:Programmation par contraintes

CSP problem examples
* cryptarithmetic
* N-queens
* map coloring
* Mastermind (dynamic)


Categories:
* Constraint Satisfaction Problems (CSP)
    * Constrained Optimization Problems (COP), with preference constraints
        * Linear Programs
            * MILP Mixed-Integer Linear Programs


Algo:


* PC-2

## `05.2` Constraint Propagation: Inference

### `05.2.1` Node Consistency


### `05.2.2` Arc Consistency

> Algorithm: AC-3 "Arc Consistency 3"

### `05.2.2` Path Consistency

> Algorithm: PC-2 "Path Consitency 2"

## `05.3` Backtracking Search for CSP
Speed-ups
Speed-up 1. Ordering
Speed-up 2. Filtering
Forward Checking
  


Filtering 1: Arc consistency
Consistency: do not violate a constraints
1-consistency (node)
2-consistency (arc): Pair of nodes
K-consistency: (1,..,K-1) -> K

Strong n-consistency


Speed-up 3. Structure

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