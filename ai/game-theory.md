# Game theory

{:toc}

### Definitions
> **Game theory**: the study of mathematical models of strategic interactions among rational agents.

> Agents:  
> Rational Agents: 

Game can be defined by:
- the initial state, s_i
- the legal actions in each state: A(s) = {s_n}
- the result of each action: R(s,a) = s'
- a terminal test: isTerminal(s) -> bool
- a utiulity function, that applies to terminal states to say who and what the final score is.

Algorithms:
- minimax
- alpha-beta search
- expetimax (with non-deterministic moves)


### Games Categorization

A | B
--- | ---
Sequential (dynamic game) | Simultaneous (static game)
Discreet | Continuous
1 Player | N-Players
Perfect Information | Imperfect Information (Partially Obervable)
Zero-sum | Non-zero-sum
Deterministic | Stochastic
Symmetric | Asym

