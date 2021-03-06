---
title: Problem Solving by Searching
tags: AIMA
---

# `03.` Problem Solving by Searching [AIMA]

- `03` Problem Solving by Searching  
    * `03.1` Problem-Solving Agents
    * `03.2` Example problems
    * `03.3` Search Algorithms
    * `03.4` Uniformed Search Strategies
    * `03.5` Informed Search Strategies (Heuristic)
    * `03.6` Heuristic functions

---

Search Problem hypothesis: 
* episodic
* single-agent
* fully-observable
* deterministic
* static
* discrete
* completely known (vs. fully observable)

## `03.1` Problem-Solving Agents


## `03.1.1` Search problems and solutions

A problem is defined as:
* __State space__: The set of possible states, $S$
    * __initial state__: $s_0$
    * __goal states__: A set (one or more) terminal states
* __Actions__: `Actions(state)` -> List< action >: list of possible actions
* __Transition model__: `Result(state, action)` -> state': 
* __Action cost function__: `Action-Cost(state, action)` -> Float:

> __Solution__: A path from the initial state to a goal state

> __Optimal solution__: Solution with the lowest path cost



* Agent
    * Simple Reflex Agent
    * Model based Reflex Agent
    * Goal based Agent
    * Utility based Agent

* Agent
    * Problem-solving Agent
    Plan a sequence of actions (path) to goal state
    Atomic representation
    * Planning Agent
    Factor or Structure representation

    * Uninformed Algorithms
    * Informed Algorithms (how far from the goal)

## `03.2` Example problems

> __Standardized problem__ vs __Real-world problem__: Benchmark for algorithms performance // Actual problem

## `03.3` Search Algorithms

> __Search algo__: `func(Problem) -> Solution | Fail`, a solution being a path or a sequence of actions | states

> __Search tree__:  
> * __Node(s)__: a state
> * __Edge(s)__: an action, from a parent node to a child | successor node

> __Generate__ vs. __Expand__ a node:   
> __Reached__: Status of a state, which has a node generated (not nec. expanded)  
> __Frontier__: set of all nodes reached 

### `03.3.1` Best-first search


### `03.3.4` Measuring problem-solving performance

> __Completeness__: guaranteed to find a solution

> __Cost optimality__: find lowest path cost

> __Time complexity__: number of states and actions?

> __Space complexity__: Memory needed

## `03.4` Uniformed Search Strategies

### `03.4.1` Bredth-first search

```
 1  procedure BFS(G, root) is
 2      let Q be a queue
 3      label root as explored
 4      Q.enqueue(root)
 5      while Q is not empty do
 6          v := Q.dequeue()
 7          if v is the goal then
 8              return v
 9          for all edges from v to w in G.adjacentEdges(v) do
10              if w is not labeled as explored then
11                  label w as explored
12                  Q.enqueue(w)
```

```
# GRAPH
def Breadth_first_graph_search(problem) -> solution:
    node = Node(state=problem.initial)
    if problem.is_goal(node.state):
        return node
    frontier = deque(node) # NODES
    reached = {node.state} # STATES, problem.initial, set
    while frontier:
        node = frontier.popleft()
        for child in problem.expand(node.state): # ??
            state = child.state
            if problem.is_goal(state):
                return child
            if state not in reached:
                frontier.append(child)
                reached.add(state)
```

```
# TREE SEARCH
# from collections import deque

def Breadth_first_tree_search(problem) -> solution:

    frontier = deque(Node(state=problem.initial, parent=None)) # NODES

    while frontier:
        node = frontier.popleft()
        if problem.is_goal(node.state):
                return node  # Goal
        frontier.append(self.expand(problem, node))

    return None  # Fail

    def expand(problem, node):

        nodes = []
        actions = problem.actions(node.state)
        for action in actions:
            state = problem.result(state, action)
            node_ = Node(state=state, parent=node)
            nodes.append(node_)

        return nodes

```


## `03.5` Informed Search Strategies (Heuristic)

## `03.6` Heuristic functions

> Subproblem  
> Pattern database  
> Disjoint pattern database  

### `03.6.4` Generating Heuristic with Landmarks

> Precomputation  
> Landmark Point

### `03.6.6` Learning heuristics from experience

> Features: Function $f(state)$: as a predictor of the goodness of the state

Heuristic as a Linear combinations of features: $ h(node) = c_1 f_1(n) + c_2f_2(n) $.  
The heuristic approximate the number of steps | distance to solution | path cost, when using A* algo.
