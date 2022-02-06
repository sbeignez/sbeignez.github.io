# AIMA.6: Adversarial Search and Game



## Minimax algorithm

Minimax optimizations
* Alpha-Beta pruning
* Move ordering
* Transposition tables


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

Expetimax