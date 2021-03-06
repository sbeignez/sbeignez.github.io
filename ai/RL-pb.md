# RL Messy notes


L1:  
AI: "Maximize your expected utility"


Memory and sim:  
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
* Deterministic | stochastic
* 1 Player | N Players
* Zero Sum | Non-ZS
* Perfect informantion (can you see the state) | Imperfect (poker)


Solution:
Deterministic | Stochastic
--- | ---
Search | Game
Solution | Strategy(policy)
Sequence | lookup table or function(s)

## Formalization (MDP)

* STATES S = [s1, s2, .., sn]
    * all_states() -> [s]
    * START state(s)
        * initial_state() -> s0 : unique
        * start_state_distribution : multi
    * TERMINAL
        * all_terminal_states() -> [s]
        * isTerminal(S) -> Bool
* PLAYERS P = {P1, ..., Pn}
* ACTIONS
    * Possible Actions: Action(Player,State) -> A+
* TRANSITION / SUCCESSOR: Successor function, Transition Function
    * successor(s,a) -> a : if deterministic
    * transition(s,a,s') -> [0,1] : if non-deterministic
* REWARD / Terminal Utility
    * utility(s,p) -> Reward for 1 player, non-zero sum 
    * reward(s,a,s') -> r (reward)

Hyperparameters
* DISCOUNT FACTOR \gamma
    * Why? 
* HORIZON H (max time t in [0, H])

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

Expectimax Pruning?
* no, except we knows some bounds on values


#### Proba (review)
Random variable, Probability distribution, ..
Distrubution: Unifom, or else?
Expectation: Expected value of a function of a randon variable = the average, weighted, by the probability distribution over all the outcomes

Uncertainty vs. Lack of knowledge of opponent model

Informed proba
