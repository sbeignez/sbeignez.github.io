# 06: Adversarial Search and Games [AIMA]

- `06` Adversarial Search and Games  
    * `06.1` Game Theory
    * `06.2` Optimal Decision in Games
    * `06.3` Heuristic Alpha-Beta Tree Search
    * `06.4` Monte Carlo Tree Search
    * `06.5` Stochastic Games
    * `06.6` Partially Observables Games
    * `06.7` Limitation of Game Search Algorithms

---

## `06.1` Game Theory

Approches for Multi-agents environments:
* agents as part of the environment. (RL?)
* agents as an aggregate: **Economy**
* agents as adversaries with strategy: **Adversarial search**



## `06.2` Optimal Decision in Games


## `06.2.1` The Minimax search algorithm



Pseudo-code

``` 
def MINIMAX(game, state) -> action:


def MAX(game, state) -> utility, action:
    if game.IS_TERMINAL(state):
        return game.UTILITY(state, player), None
    v, move = - math.inf, None
    for action in game.ACTIONS(state):
        v_, action_ = MIN(game, game.RESULT(state, action))
        if v_ > v:
            v, action = v_, action_
    return v, action

def MIN(game, state) -> utility, action:
    # same
    pass


```

Minimax optimizations
* Alpha-Beta pruning
* Move ordering
* Transposition tables

## Expectimax Algorithm