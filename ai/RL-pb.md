## id

checker

pac-man (berkeley 2015, 

tictactoe

snake and scales


L1:  
AI: "Maximize your expected utility"


Memory adn sim:  
Machine-Learning based AI  
Simulation based AI  

Agent = entity that perceives and acts, + rational = maximize utility


Part: 1 Makign decisions
    Fast search, planning
    CSP: Constraint satisfaction problems
    adversarial and uncertain search)
Part 2: reasoning under uncertainty (bayes' nets, decision theory, ML)


# [Lecture6 ](https://www.youtube.com/watch?v=-Il2oJoItaI)

Deterministic Games

## Type of games, Classification:
* Deterministic or stochastic
* Players: 1, 2, +
* Zero Sum ?
* Perfect informantion (can you see the state) ../poker

Solution or strategy(policy)
sequnece // lookup table or function(s)

## Formalization

* STATES S = {...}
* PLAYERS P = {P1, ..., Pn}
* ACTIONS
    * Possible Actions: Action(Player,State) -> A+
* Transition Function, or successor function
    * SxA --> S
* Terminal Test
    * isTerminal(S) -> Bool
* Terminal Utility
    * utility(S,P) -> Reward

Solution: 
* $ POLICY \pi: S \rarr A $

Zero-sum games: Adversarial, Pure Competition (opposite utility). Min/Max only 1 utility.
General Games: Independent utilities to optimize 

# Adversiarial Search

See the future, steps, ..

1) Single-Agent Trees

Value of the states:
- the best achievable outcome from that state
- can use NN ?!

Terminal states $$ V(s) = Reward \text{  (known, cf reward tale)} $$  
Non-Terminal states: $$ V(s) = Max_{s'\in children(s)} V(s')$$

2) Adversarial game-tree

Adversarial Search MiniMax

* max at agent's control / min at opponent's control

$$ V(s) = \text{if } isPayer(s): max_{s'\in succ} V(s'), \text{if } not isPayer(s): min_{s'\in succ} V(s') $$


```
def max-value(state s)
    init v = -inf
    for each s' in succ(s):
        v = max( v , min-value(s'))

def min-value(state s):
    init v = + inf
    for each s' in succ(s):
        v = max( v , max-value(s'))

```
multual recursion


```
def value(state s)
    if s is terminal, return R(s)
    if next agent is MAX: return max-value(s)
    if next agent is MIN: return min-value(s)

def max-value(s)
    v = - inf
    v = max( [ v] + [ value(s') for s' in succ(s) ] )

```

DFS - deppth First Search  
b: branches (2-4)
m: layers (c+r = 20)
$$O(b^m)$$ 

Adversarial? = Opponent agent always take the best move

---

Ressource Limits

Solution:
* Deepth-limited search
* Replace terminal utilities with an evaluation function for non-terminal states !!
(can use function, or NN approximator)

Evaluation function  
$$ Eval(s) = w1*f1(s) + .. + wn*fn(s) $$
lot of features f, linear compunations
and weights: by Machine Learning 

eX:  
return score  

danger: Replanning agents
Solution: if same values (2 nodes in max), take the one with mean is higer

Game Tree Prunning

\alpha \beta

meta-reasoning: (computing about what to compute)
* node ordering


# Lecture 7: [Uncertainty and Utilities](https://www.youtube.com/watch?v=M98BM_yJPNw)

Uncertain outcomes

Worst case vs. Average case

Outcomes controlled by chance, not adversary. Out of our control.
ex: roll dices, ..
explicit randomness, unpredictable (noise), optimal with risk of failure

Distrubution: Unifom, or else?


### Expectimax Search

Chance node

Weighted average value
Expected utility


```
def value(state s)
    if s is terminal, return R(s)
    if next agent is MAX: return max-value(s)
    if next agent is EXP: return exp-value(s)

def exp-value(state s)
    init v = 0
    for each s' in successors of state s
        p = probability(succ(s)=s')
        v+= p * value(succ(s)=s')
``` 
