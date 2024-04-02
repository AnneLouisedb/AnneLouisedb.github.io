# Game Theory notes
[play game](https://gamesinterface.streamlit.app/)
### von Neumann-Morgenstern axioms
- **Completeness**
  
Completeness assumes that an individual has well-defined preferences and can always decide between any two alternatives. For every $A$ and $B$, either $A\succeq B$ or $A\preceq B$, or both. This means that the individual prefers $A$ to $B$, $B$ to $A$, or is indifferent between $A$ and $B$. 

- **Transitivity**
  
Transitivity assumes that, as an individual decides according to the completeness axiom, the individual also decides consistently. For every $A, B$, and $C$ with $A\succeq B$ and $B\succeq C$, we must have $A\succeq C$.

- **Independence of Irrelevant Alternatives**

IIA pertains to well-defined preferences as well. It assumes that two gambles mixed with an irrelevant third one will maintain the same order of preference as when the two are presented independently of the third one. For every $A, B$ such that $A\succeq B$, the preference $tA+(1-t)C\succeq tB+(1-t)C$ must hold for every lottery $C$ and real $t\in [0,1]$.

## Savage
to do : Certainty Equivalence by De Finetti (1970) and Savage (1971).

Savage (1954) first introduced Expected Utility theory for decision under uncertainty, which was later extended by Anscombe and Aumann (1963) to acts over lottery outcomes.
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

# Bayesian game

[Strategic Distinguishability](https://www.sciencedirect.com/science/article/abs/pii/S0022053117300030)
According to the paper there are two reasons for interdependence of types.
1. informational reasons
2. psychological reasons
Types define different information, preferences, beliefs, or attributes that can distinguish one individual or agent from another.


A type of agent is defined by the belief that one has about the other agent's types. 
In addition to the type set, each agent has a utility function specifying her utility over outcomes, given each profile of agents' types. Such utility functions are the private information that agents hold which affect their their decision-making or strategic behavior.

The authors assume agents preference can be represented by expected utilities that depend on the agent's types profile. 


#### Bayesian Game
- Players
- Actions sets $A_i$
- Type Sets $\Theta_n$
- Payoff function: $A x \Theta -> R$ (utility funcion)
- Beliefs $p(\theta | \theta)$ - condtional probability on types of players
- Strategies (may be pure or mixed)
- Expected utilityes, $\sum (p(\theta | \theta)u(s(\theta))s(\theta); \theta, \theta)$

The bayesian nash equilibrium is set of strategies - maximizes expected utility given the strategies of other playes
- know your own payoff as private information
- there is uncertainy about other players payoffs and their actions
There is (1) payoff uncertainty, and (2) strategic uncertainty.

#### Interdependent preferences
1. Each type has a hierarchy of beliefs about the private states. (A type space based on the profile of the private states)
2. The hierarchy about beliefs on the private states "hierarchy of interdependent preferences" is a first order preference. (preference over lotteries)
3. Second order belief (Anscombe- Aumann) represents a preference over acts over the oponents first order preferences. 

Two types are strategically distinguishable if and only if they have different hierarchyies of beliefs 
about the private states and thus if they have differeent hierarchies of interdependent preferences. 

Abreu and Matsushima (1992), characterize virtual Basian social choice functions for a type space by iterated deletion of strictly dominated strategies. 
Types with the same hierarchies of interdependent preferences give the same outcome in social choice functions, as introduced by Abreu and Matsushima (1992). 

**Method**
- ask agents to report first orders of preferences (of outcomes)
- randomizes over which component of the mechanism is used to select the outcome
- report n-th order preferneces
- the components give each other agent an incentive to truthfully report his (n+1)th and higher order preferences. 
- we have arbitary type spaces and agents' preferences over outcomes may be arbitrarily linked
- the paper develops a robust scoring rule that incentivies to report the n-th order prefectness truthfully if others report their (n-1)th and lower order preferences truthfully. 


## Harsanyi 1967: Games with Incomplete Information
- Bayesian games
  
## Kuhn 1953: Extensive games and the problem of information

## Auction and Bidding

### Variation of the VCG mechanism
To derive a mechanism for this auction that satisfies DSIC (Dominant-Strategy Incentive Compatibility), EFF (Efficiency), and runs in polynomial time in $n$ and $m$, we can use a variation of the VCG mechanism. Since this is a VCG mechanism, it can be defined very generally, and is always DSIC and welfare-maximizing.

Since every item can only be given to at most one player, welfare-maximization is exactly the maximum-weight bipartite matching problem

- *Bid Collection*: Each player submits bids $b_{ik}$ for every item $k \in M$.
  
- *Compute an allocation* corresponding to a maximum-weight bipartite matching, using
the $b_{ik}$’s as edge weights. The bipartite matching problem can be solved in polynomial time using linear programming.

- *Social welfare*: $SW(b) = \sum_{i = 1}^{n} v_i(S_i)$ where $S_i$ is the allocation for bidder $i$, we maximize this over all partitions of m.

- *Determination of Allocations*: For each player $i$, calculate the allocation that maximizes $v_i(S)$ among all possible bundles $S \subseteq M$ based on their submitted bids. Assign each item to the player who values it the most, ensuring that each player receives at most one item, and items are allocated once.

- *Payment Calculationz*: Each bidder is charged their externality on the other bidders — the welfare loss to the others caused by its presence. The price that is paid by player $i$ is:
   
$p_i =  \sum_{j \not = i}v_j(M_{-j}(j)) - \sum_{j \not = i}v_j(M(j))$

Where M is the VCG outcome, and the welfare-maximizing matching $M_{-i}$ that leaves i unmatched. If an item is unsold then $p(i) = 0$

#### DSIC
Let's prove that every player $i$ maximizes their utility function $u_i$ by bidding truthfully, i.e. bidding $b_i = v_i$ is a dominant strategy for every player $i \in N$, i.e.,
$u_i(v_i, b_{-i}) \geq  u_i(b_i, b_{-i}) \quad \forall b_{-i} \forall b_i$

where $b_{-i}$ refers to an arbitrary fixing of the other players' bids.

It is explained in Lecture Notes' Theorem 4.2 that any VCG mechanism has the DSIC property.

#### EFF
We have to show that under truthful bidding, the allocation x(b) computed by M(b) maximizes the social welfare, i.e.

$\sum_{i \in N} v_ix_i(b) \geq \sum_{i \in N}v_i x, x^*_i \quad \forall x^* \in X$

This is trivial, under no other bidding strategy can any player $i$ further improve the total social welfare.

#### Run in Polynomial time
This mechanism computes the output in polynomial time (in the input size).

Since this VCG mechanism can determine its maximum social welfare in polynomial time through the use of linear programming, the entire mechanism can be done in a polynomial amount of operations.



### The k-Vickrey Auction
- *Bid Collection*: Each bidder $i$ submits a bid $b_i$, representing their valuation for one of the $k$ identical items.
    
- *Determination of Winners*: Bidders are ranked by their submitted bids in descending order. Any ties are resolved arbitrarily. The top $k$ bidders are the winners of the auction. Any ties are resolved arbitrarily. In the case of a tie, unit j is randomly assigned among the bidders who submitted the highest bid.

- *Payment Calculation*: Each winning bidder is obligated to pay the amount of the first losing bid, i.e. $b_{k+1}$. As such, we can define the utility of any player $i$ with bid profile $b_i$ to be $u_i = x_i \cdot (v_i - b_{k+1})$, where $x_i = 1$ if bidder $i$ has won an item and $x_i = 0$ otherwise.

- *Item assignment*: Allocate one of the $k$ identical items to each winning bidder.


#### DSIC
Let's prove that every player $i$ maximizes their utility function $u_i$ by bidding truthfully, i.e. bidding $b_i = v_i$ is a dominant strategy for every player $i \in N$, i.e.,
$u_i(v_i, b_{-i}) \geq  u_i(b_i, b_{-i}) \quad \forall b_{-i} \forall b_i$

where $b_{-i}$ refers to an arbitrary fixing of the other players' bids.

Two cases are possible, for each case it goes that $u_i = \max(0, v_i - b_{k+1})$.

If $v_i < b_{k+1}$, then the optimal utility is 0, which can be achieved with a truthful bid. Placing a bid $b_i > v_i$ would result in a negative utility $u_i$ and any bid $b_i < v_i$ would also result in $u_i = 0$, so in this case there is never a utility benefit to bidding untruthfully.

In the other case $v_i \geq b_{k+1}$, the optimal utility is $v_i - b_{k+1}$. Bidding above $v_i$ will not change this utility, as $b_i$ is not the value that will be paid, while bidding below $v_i$ leads to the risk of not winning the auction and thus obtaining $u_i = 0$.

#### EFF
We have to prove that under truthful bidding, the allocation x(b) computed by M(b) maximizes the social welfare, i.e.
$\sum_{i \in N} v_ix_i(b) \geq \sum_{i \in N}v_i x, x^*_i \quad \forall x^* \in X$

This is trivial for a k-Vickrey auction. As truthful bidding ensures that the $k$ bidders with the highest valuations are assigned an item, there is no losing player left with a valuation that would improve the social welfare.

#### Polynomial time
M(b) computes the output $(x(b), p(b))$ in polynomial time (in the input size). 

For the first step, $n$ operations are made to obtain each bid. These are then sorted, which can be done in $n^2$ operations. Then $k+1$ operations are needed to pick the top $k+1$ bids and finally, $k$ items are handed out. In total, this requires $n^2 + n + 2k +1$ operations. 


#### Problem 3b
*Consider the combinatorial auction setting, where the set of players is N and the set of items is M. Assume that the auctioneer runs the VCG mechanism (Algorithm 8 in the Lecture Notes). Show that the payments $(p_i) i \in N$ computed by the VCG mechanism satisfy that for every player $i \in N$ $0 \leq p_i \leq b_i(a^*)$*
**Proof:**

The price $p_i$ of player $i$ is defined as:

$p_i = b_i(a^*) - (\max_{a \in O}\sum_{j \in N} b_j(a) - \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a))$

Since $a* = \arg \max_{a \in O} \sum_{i \in N}v_i(a)$ (maximizing the sum over all bids) and the assumption that in this setting the dominant strategy for every player is to bid $b_i(S) = v_i(S)$, we have:

$p_i = b_i(a^*) - (\sum_{j \in N} b_j(a^*) - \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a))$

$p_i = -\sum_{j \in N, j \not = i} b_j(a^*) + \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a))$

If $a = a*$, then $p_i = 0$. If $a \not = a*$, then the second term will be bigger than the first, by the maximization of $a \in O$. Therefore $p_i > 0$. We have shown $p_i \geq 0$ for all $i \in N$. This means the seller is prohibited from paying the bidders.

Secondly we need to show: $p_i \leq b_i(a^*)$ for every $i \in N$.

By observing equation 1, we need to show:

$(\max_{a \in O}\sum_{j \in N} b_j(a) - \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a)) \geq 0$

Or equivalent: 

$\max_{a \in O}\sum_{j \in N} b_j(a) \geq \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a)$

We need to show that $i$'s contribution to SW cannot be negative. 

1. If players $j \not = i$ bid the same as player $i$ would bid on its items obtained in allocation $a^*$, then the sum over the bids in the respective allocations would be the same, such that $(\sum_{j \in N} b_j(a^*) - \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a)) = 0$.
2. If the other bidders $j \not = i$ bid less (on the items allocated to $i$ in $a^*$) than $i$ would bid, then $\max_{a \in O}\sum_{j \in N} b_j(a) \geq \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a)$.

We show that Eq 4 holds for both cases. If bidders $j \not = i$ would bid higher on the items obtained by $i$ in $a^*$, we would have: 

$\max_{a \in O}\sum_{j \in N} b_j(a) \leq \max_{a \in O} \sum_{j \in N, j \not = i}b_j (a)$

But this contradicts the efficiency of $a^*$ since the items would not be allocated to $i$ in $a^*$ if there existed another bid higher than player $i$'s bid.

We have shown that the payments $(p_i) i \in N$ computed by the VCG mechanism satisfy that for every player $i \in N$, $0 \leq p_i \leq b_i(a^*)$.



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


- ADD: Prove that every coordination game is an exact potential game.

### Congestion game
We consider a convex combination between the social cost and the original. The potential function by Rosenthal:

$\Phi (s) = \sum_{e \in E} \sum^{x_e}_{k=1}c_e(k)$

In the congestion game we assume $c_e(k) = k$


Where,

$\Phi (s) = \sum_{e \in E} \sum^{x_e(s)}_{k = 1}k$


$\Phi^{\alpha}(s) = (1 - \alpha) \Phi (s) + \alpha SC(s)$
 

$\Phi^{\alpha}(s) = (1 - \alpha) \sum_{e \in E} \sum_{k=1}^{x_e(s)} k + \alpha SC(s)$
        
The sum of the first n natural numbers of an arithmetic series is $\frac{n(n-1)}{2}$, hence:

$= (1 - \alpha) \sum_{e \in E} (\frac{x^2_e (s) + x_e(s)}{2} )+ \alpha \underbrace{\sum_{e \in E}x^2_e (s)}_{= \sum_{e \in E} (\sum_{k = 1}^{x_e(s)} x_e(s))}$

$= \frac{(1 - \alpha)}{2} \sum_{e \in E} (x^2_e (s) + x_e(s)) + \alpha \sum_{e \in E}x^2_e (s)$

$= \frac{(1 - \alpha)}{2} \sum_{e \in E} x^2_e (s) + \alpha \sum_{e \in E}x^2_e (s)  +\frac{(1 - \alpha)}{2}\sum_{e \in E} x_e(s)$
We can combine the first and second term,
    
$=  \frac{(1 - \alpha)}{2}\sum_{e \in E}x_e (s) + \underbrace{ \frac{(1 + \alpha)}{2} }_{ = \frac{(1 - \alpha)}{2} + \alpha }\sum_{e \in E}x^2_e (s)$
  
$\Phi^{\alpha} (s) =   \frac{(1 - \alpha)}{2}\sum_{e \in E}x_e (s) +  \frac{(1 + \alpha)}{2} SC(s) \quad (1)$

We obtain, 

$ \frac{(1 + \alpha)}{2}SC(s) \leq \Phi^{\alpha}(s) \leq SC(s)$
    
First inequality can be explained by Eq 1. The second inequality 
$\Phi^{\alpha}(s) \leq SC(s)$
can be shown as follows. We have \(x_e(s) \geq 1\). It is evident that for
$\alpha \in [0,1]$:

$\frac{(1 - \alpha)}{2} \sum_{e \in E} \left(x_e(s)}\right) <  \frac{(1 + \alpha)}{2}\sum_{e \in E} x^2_e(s).$

The inequality $\Phi^{\alpha}(s) \leq SC(s)$, shows that the upper bound is a scenario where $\alpha = 1$. 


By theorem 2.10 of the lecture notes we know the following,
Consider an ordinal potential game
$\Gamma = (N, (X_i)_{i\in N}, (c_i)_{i\in N})$ 
with potential function $\Phi$ and let 
$SC : X \rightarrow \mathbb{R}_{\geq 0}$ 
be a social cost function. Suppose there exist some $\alpha, \beta > 0$ such that the potential function $\Phi$ satisfies for every $x \in X$:

$\frac{1}{\alpha} \cdot SC(s) \leq \Phi(x) \leq \beta \cdot SC(x).$

Then $POS (\Gamma^{\alpha}) \leq \alpha \beta$
In this case we have: 

$\frac{(1 + \alpha)}{2}SC(s) \leq \Phi^{\alpha}(s) \leq SC(s)$
    
Using our findings and the identity above: 

$POS (\Gamma^{\alpha}) \leq \frac{1}{\frac{(1 + \alpha)}{2}} \cdot 1  = \frac{2}{1 + \alpha}$

## Shapley 1952: Fairness and Stability in coalitional games
- Shapley value


# Resources
[Nash 1951](https://www.jstor.org/stable/1969529?origin=crossref)

[Rosenthal 1971](http://dx.doi.org/10.1007/BF01737559)

[Wakker and Deneffe 1996](https://repub.eur.nl/pub/23096/Eliciting_1996.pdf)

[Harsanyi 1967](http://dx.doi.org/10.1287/mnsc.1040.0270)

[Kuhn 1953](https://books.google.nl/books?id=HyTpw6H5syUC&lpg=PA46&dq=extensive%20games%20and%20the%20problem%20of%20information&hl=nl&pg=PA46#v=onepage&q=extensive%20games%20and%20the%20problem%20of%20information&f=false)

[Shapley 1952](https://apps.dtic.mil/sti/pdfs/AD0604084.pdf)
