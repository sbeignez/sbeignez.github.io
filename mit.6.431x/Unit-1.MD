# Probability. Unit 1. Sample Space and Probability

## 1.1.3 Sample space

> Sample space, set of all possible outcomes

- Set of possible outcomes, $\Omega$
    - Mutually exclusive 
    - Collectively exhaustive
    - At right granularity, with relevant features
- Likelihood of outcomes

> Discrete & Finite / Continuous & Infinite

> Experiment, Probabilistic experiment

> an **outcome** is a possible result of an experiment  
> an "outcome" is an element of the set "sample space"

Experiment with stages
sequenctial description: Tree


## 1.1.7 Probability Axioms

P(A), read: Probability of set A

> Event: A subset of the sample space, or a set of outcomes 

Individual outcomes of continuous space have all a probability = 0.  
Probability is assigned to events (but not to individuals outcomes)

Axioms

> Non-negativity: $ P(A) \ge 0 $

> Normalization: $ P(\Omega) = 1 $

> (Finite) additivity: $ \text{If } A \cap B = \emptyset \text{, then } P(A \cup B) = P(A) + P(B) $

$ A \cap B = \emptyset$: events (and sets) are "disjoint"

$ P(A \cup B) = P(A) + P(B) - P( A \cap B)$

Consequences:

> $ P(A) \le 1 $   

> $ P(\empty) = 0 $   

> $ P(A) + P(A^c) = 1 $   

> Complement of event

$ A^c $ is the **complement** of event A, such as $ A \cup A^c = \Omega $, and $ A \cap A^c = \empty $

> $ P(A \cup B \cup C) = P(A) + P(B) + P(C)$, if the 3 set are disjoint

> $ \text{If } A_1, ..., A_k \text{ are disjoint, then } P(A_1 \cup .. \cup A_k) = \sum_{i=1}^k P(A_i)$

## 1.1.11 More Properties

> $ \text{If } A \subset B \text{, then } P(A) \le P(B)$

> The union bound: $ P(A \cup B) \le P(A) + P(B)$

> $ P(A \cup B \cup C) = P(A) + P(B \cap A^c) + P( C \cap B^c \cap A^c)$

## 1.1.13 Finite ex.

Define/specify a probability law, probability assignment.

> Discrete uniform law

* $\Omega$, with n **equally likely** elements
* A, k elements
* all elements has a probability of $1/n$

> $ P(A) = k/n $ 

#### Exercices:  
The event of interest is { , , }

## 1.1.15 Continuous ex.

> Uniform probability law

* Probability = Area

Probability calcualtion steps:
1. Specify the sample space
2. Specify a probability law
3. Identify an event of interest
4. Calculate

## 1.1.17 Countable additivity

Discrete and infinite sample space

Geometric serie:
$$ \sum_{i=0}^{\infin} a*n^i = {a \over (1 - n)}$$

> Countable Additivity Axiom  
> $ If A_1, A_2, .. $ is an infinite **sequence** of disjoint events,  
> $ then P(A_1 \cup) = P(A_1) + P(A_2) + P(A_3) + ... $

sequence: countable 

## 1.1.21

What is Probability?
* Frequency
* Description of beliefs
* Betting preference

Framework for analysing phenomena with uncertain outcomes

Real world --DATA--> Inference/Statistics --MODELS-> Probability theory --PREDICTIONS/DECISIONS-> Real world



# Solved Problems

## 1.

$$ P( (A \cap B') \cup (A' \cap B)) = P(A) + P(A) - 2 * P(A \cap B) $$

## 2. 