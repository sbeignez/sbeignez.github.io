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

MiniMax values
* max at agent's control / min at opponent's control

$$ V(s) = \text{if } isPayer(s): max_{s'\in succ} V(s'), \text{if } not isPayer(s): min_{s'\in succ} V(s') $$