# Game Theory notes

### von Neumann-Morgenstern axioms
- **Completeness**
  
Completeness assumes that an individual has well-defined preferences and can always decide between any two alternatives. For every $A$ and $B$, either $A\succeq B$ or $A\preceq B$, or both. This means that the individual prefers $A$ to $B$, $B$ to $A$, or is indifferent between $A$ and $B$. 

- **Transitivity**
  
Transitivity assumes that, as an individual decides according to the completeness axiom, the individual also decides consistently. For every $A, B$, and $C$ with $A\succeq B$ and $B\succeq C$, we must have $A\succeq C$.

- **Independence of Irrelevant Alternatives**

IIA pertains to well-defined preferences as well. It assumes that two gambles mixed with an irrelevant third one will maintain the same order of preference as when the two are presented independently of the third one. For every $A, B$ such that $A\succeq B$, the preference $tA+(1-t)C\succeq tB+(1-t)C$ must hold for every lottery $C$ and real $t\in [0,1]$.

## Savage

Preference Independence is a fundamental axiom that states preferences should remain consistent regardless of how a decision problem is framed. In other words, if two acts, A and B, have a consistent preference relation across all possible states of the world, this preference relationship should hold regardless of other acts or contextual factors.

According to Savage, if a weak preference relation, denoted as $\succsim$, satisfies Savage's axioms, then the following important conclusions can be drawn:

1. **Unique Probability Function $(P)$**: The agent's confidence in the actuality of the states in the state space $(S)$ can be represented by a unique (and finitely additive) probability function denoted as $P$.

2. **Utility Function $(u)$**: The strength of the agent's desires for the ultimate outcomes in the outcome space $(O)$ can be represented by a utility function, denoted as $u$. This utility function is unique up to positive linear transformations.

3. **Expected Utility Function**: The pair $(P, u)$ gives rise to an expected utility function, denoted as $U$, which represents the agent's preference for the alternatives in the set $F$. Formally, for any two alternatives $f, g, \in F$, the following relation holds:

$f \succsim g \Leftrightarrow U(f) \leq U(g)$


Note: utility functions are often easier to determine than beliefs (probability functions). Moreover, both probability and utility functions can be derived from preference orderings. While they are unique, it's important to note that the utility function can be transformed linearly in a positive manner without altering the underlying preferences.

## Eliciting von Neumann-Morgenstern Utilities
Decision analysis often involves making choices under uncertainty, where individuals or decision-makers assign values to different outcomes based on their preferences and beliefs. The concept of vNM utilities plays a crucial role in quantifying these preferences, allowing for rational decision-making in the face of uncertainty.
The paper by Wakker and Deneffe 1996 covers the following methods for eliciting utilities under uncertainty.
#### Certainty Equivalent (CE) Method
1. Select two extreme outcomes, denoted as M and m, such that all outcomes of interest lie between them.
2. Determine the outcome CE(p) that renders the individual indifferent to (0, p; M).
3. The CE method is often applied iteratively in a bisection form to elicit utilities for various probabilities.
#### Probability Equivalence (PE) Method

#### Tradeoff Method

   

  
    

# Resources
[Nash 1951](https://www.jstor.org/stable/1969529?origin=crossref)

[Rosenthal 1971](http://dx.doi.org/10.1007/BF01737559)

[Wakker and Deneffe 1996](https://repub.eur.nl/pub/23096/Eliciting_1996.pdf)
