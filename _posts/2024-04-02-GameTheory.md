# Game Theory notes

### von Neumann-Morgenstern axioms
- **Completeness**
  
Completeness assumes that an individual has well-defined preferences and can always decide between any two alternatives. For every $A$ and $B$, either $A\succeq B$ or $A\preceq B$, or both. This means that the individual prefers $A$ to $B$, $B$ to $A$, or is indifferent between $A$ and $B$. 

- **Transitivity**
  
Transitivity assumes that, as an individual decides according to the completeness axiom, the individual also decides consistently. For every $A, B$, and $C$ with $A\succeq B$ and $B\succeq C$, we must have $A\succeq C$.

- **Independence of Irrelevant Alternatives**

IIA pertains to well-defined preferences as well. It assumes that two gambles mixed with an irrelevant third one will maintain the same order of preference as when the two are presented independently of the third one. For every $A, B$ such that $A\succeq B$, the preference $tA+(1-t)C\succeq tB+(1-t)C$ must hold for every lottery $C$ and real $t\in [0,1]$.

## Savage
to do : Certainty Equivalence by De Finetti (1970) and Savage (1971).

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


## Harsanyi 1967: Games with Incomplete Information
- Bayesian games
  
## Kuhn 1953: Extensive games and the problem of information

## Auction and Bidding

### Price of Anarchy
Consider the following scheduling game: We are given a set of jobs $N = [n]$ that need to be processed on a set of machines $M = [m]$. Every job $j \in N$ has a processing time $p_j > 0$, which defines the amount of time that $j$ needs to be processed. A schedule $x = (x_1, \ldots, x_n) \in M^n$ assigns each job $j \in N$ to a machine $x_j \in M$ on which it is processed. The load $L_i(x)$ of a machine $i \in M$ with respect to a given schedule $x$ is defined as the total processing time of all jobs that are assigned to $i$, i.e. $L_i(x) = \sum_{j \in N:x_j=i} p_j.$

Here, the interpretation is that each job $j \in N$ corresponds to a player who chooses a machine $x_j \in M$ to minimize her own completion time. The completion time $C_j(x)$ of player $j \in N$ with respect to a given schedule $x$ is defined as the load of the machine to which player $j$ is assigned, i.e., $C_j(x) = L_i(x)$ with $i = x_j$. We define the social cost $SC(x)$ of a schedule $x$ as the maximum load of a machine, i.e.,

$SC(x) = \max_{i \in M} L_i(x).$ - A social optimum is a schedule that minimizes the social cost.
Consider a scheduling game with m = 2 machines and n = 4 jobs. Let p1 = p2 = 2 and p3 = p4 = 1. The pprice of anarchy of this instance can be determined as follows:
Consider a NE of $\Gamma$ with the worst posisble social cost, which is the case where $L_1 = p_1 + p_2$, and $L_2 = p_3 + p_4$. ($x = \{1,1,2,2 \}$) No one has the incentive to switch and the social cost is $SC = L_1 = 4$ Consider the optimal SC where jobs are divide evenly over the two machines s.t. $SC = L_1(x^*) = L_2(x^*) = 3$. ($x^* = \{1,2,1,2 \}$)

$POA(\Gamma) = \frac{SC_{NE}}{SC_{opt}} = \frac{4}{3}$

The example can be generalized to $m$ jobs. Assume there are $m$ jobs of weight $m$, and $m$ jobs of weight 1. Note that the total number of jobs is 
$n = 2m$.
The OPT is  $SC(x^*) = m+1$
, since for each machine you can assign the weight $m$ plus the weight of a job of weight 1. 
There is a NE where two jobs of time $m$ are assigned to the same machine, lets say the first machine st. 
$L_1 = 2m$, and the remaining $m-2$ jobs of time $m$ choose machines $2, 3, 4, ..., m-1$, and all the jobs of time 1 choose machine $m$.
$(L_m = \sum^m 1 = m )$
No one has the incentive to switch and the social cost is equal to $SC = L_1 = 2m$. In this case the 

$POA(\Gamma) = \frac{SC(x)}{SC(x^*)} \geq \frac{2m}{m+1}$

### Interpolating strategies
 $c^{\alpha}_i = \alpha \cdot SC(x) + (1 - \alpha) \cdot c_i(x) \quad \forall i \in N$
As alpha increases, each players cost function is closer to the social cost. This means the higher the alpha, the more players tend towards the social cost optimal solution. The players cost is a weighted combination of the indidividual selfish cost $c_i (s)$ and the social cost $SC$. The parameter $\alpha$ accounts for the degree of altruism for player i.  When $\alpha = 0$, the player is completely selfish. When $\alpha = 1$, the player is completely altruistic. "altruism" refers to the degree to which a player is willing to prioritize the overall social cost over their individual self-interest.

### Congestion game
We consider a convex combination between the social cost and the original. The potential function is Rosenthal: \\

$\Phi (s) = \sum_{e \in E} \sum^{x_e}_{k=1}c_e(k)$
In the congestion game we assume $c_e(k) = k$
Where,

$\Phi (s) = \sum_{e \in E} \sum^{x_e(s)}_{k = 1}k$


$\Phi^{\alpha}(s) = (1 - \alpha) \Phi (s) + \alpha SC(s)$
 

$\Phi^{\alpha}(s) = (1 - \alpha) \sum_{e \in E} \sum_{k=1}^{x_e(s)} k + \alpha SC(s)$
        
The sum of the first n natural numbers of an arithmetic series is $\frac{n(n-1)}{2}$, hence:

$  =  (1 - \alpha) \sum_{e \in E} (\frac{x^2_e (s) + x_e(s)}{2} )+ \alpha \underbrace{\sum_{e \in E}x^2_e (s)}_{= \sum_{e \in E} (\sum_{k = 1}^{x_e(s)} x_e(s))}$

$= \frac{(1 - \alpha)}{2} \sum_{e \in E} (x^2_e (s) + x_e(s)) + \alpha \sum_{e \in E}x^2_e (s)$

$= \frac{(1 - \alpha)}{2} \sum_{e \in E} x^2_e (s) + \alpha \sum_{e \in E}x^2_e (s)  +\frac{(1 - \alpha)}{2}\sum_{e \in E} x_e(s)$
We can combine the first and second term,
    
$=   \frac{(1 - \alpha)}{2}\sum_{e \in E}x_e (s) + \underbrace{ \frac{(1 + \alpha)}{2} }_{ = \frac{(1 - \alpha)}{2} + \alpha }\sum_{e \in E}x^2_e (s)$
  
$\Phi^{\alpha} (s) =   \frac{(1 - \alpha)}{2}\sum_{e \in E}x_e (s) +  \frac{(1 + \alpha)}{2} SC(s) \quad (1)$

We obtain, 

$ \frac{(1 + \alpha)}{2}SC(s) \leq \Phi^{\alpha}(s) \leq SC(s)$
    
First inequality can be explained by Eq 1. The second inequality  $\Phi^{\alpha}(s) \leq SC(s)$ can be shown as follows. We have \(x_e(s) \geq 1\). It is evident that for $\alpha \in [0,1]$:

$\frac{(1 - \alpha)}{2} \sum_{e \in E} \left(x_e(s)}\right) <  \frac{(1 + \alpha)}{2}\sum_{e \in E} x^2_e(s).$

The inequality $\Phi^{\alpha}(s) \leq SC(s)$, shows that the upper bound is a scenario where $\alpha = 1$. 


By theorem 2.10 of the lecture notes we know the following,
Consider an ordinal potential game $\Gamma = (N, (X_i)_{i\in N}, (c_i)_{i\in N})$ with potential function $\Phi$ and let $SC : X \rightarrow \mathbb{R}_{\geq 0}$ be a social cost function. Suppose there exist some $\alpha, \beta > 0$ such that the potential function $\Phi$ satisfies for every $x \in X$:

$\frac{1}{\alpha} \cdot SC(s) \leq \Phi(x) \leq \beta \cdot SC(x).$

Then $POS (\Gamma^{\alpha}) \leq \alpha \beta$
In this case we have: 

$\frac{(1 + \alpha)}{2}SC(s) \leq \Phi^{\alpha}(s) \leq SC(s)$
    
Using our findings and the identity above: 

$POS (\Gamma^{\alpha}) \leq \frac{1}{\frac{(1 + \alpha)}{2}} \cdot 1  = \frac{2}{1 + \alpha}$

    


# Resources
[Nash 1951](https://www.jstor.org/stable/1969529?origin=crossref)

[Rosenthal 1971](http://dx.doi.org/10.1007/BF01737559)

[Wakker and Deneffe 1996](https://repub.eur.nl/pub/23096/Eliciting_1996.pdf)

[Harsanyi 1967](http://dx.doi.org/10.1287/mnsc.1040.0270)

[Kuhn 1953](https://books.google.nl/books?id=HyTpw6H5syUC&lpg=PA46&dq=extensive%20games%20and%20the%20problem%20of%20information&hl=nl&pg=PA46#v=onepage&q=extensive%20games%20and%20the%20problem%20of%20information&f=false)
