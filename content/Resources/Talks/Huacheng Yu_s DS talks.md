---
{"publish":true,"title":"Yu's DIMACS talks","created":"August 8-11, 2022","modified":"2025-05-24T17:36:31.114+01:00","published":"August 8-11, 2022","cssclasses":""}
---

#talk

# Part 1: Static DS LBs 
- Cell probe model (w,s,n)
	- Memory divided into $s$ cells. 
	- Each cell hold $w$ bits. 
	- can access a cell in a unit time
	- computation is free
	- time/resorce = # cells probed
	- n = # queries
		- $w = \theta(\log n)$. 
		- $w =1$ bit probe model.
		- $w = \omega(\log n)$ external memory case.
Talk outline
- Techniques Static DS LB
- Techniques Dynamic DS LB

Running example: 
> ***Polynomial evaluation.*** 
>	***Data:*** $p(x)$ of deg $n-1$ 
>	***queries:*** $x \in \mathbb{F}_q$ we must return $p(x)$.
>    ***task:*** process it into a data structure of size $s$. 

- Non-trivial upper bound for polynomial evaluation [Umans]
	- $s = n^{1+o(1)}$, $t_q = \log n \cdot \log q$ ($q$ = filed size).
	- Fast fourier 

### Reduction from communication complexity 

##### [[[Miltersen]], [[N. Nisan]], [[S. Safra]] , [[Avi Wigderson]]'94]
- Alice has $x$ ,
- Bob has a polynomial $p$,
- There is a protocol where Alice sends $t_q(\log s)$ bits and Bob sends $t_qw$ bits of communication. 
###### Communication ***lower bound*** 
> ***Claim***
> - Either Alice sends $\geq \log q -c$ bits or 
> - Bob sends at $\geq 2^c \log q$ bits.    

This technique cannot prove better than $\Omega(\log |Q|/\log s)$.  

##### Patrascu and Thorup '06

Alice: $x_1, \dots ,x_k$
Bob: polynomial $p$

Communication cost: 
	Alice sends $t_q.\log \binom{s}{k}$ = $O(t_q\log \frac{s}{k})$ 
	Bob sends $t_q\cdot  k\cdot  w$ bits.

> [!Note] ***Claim***:
> Either Alice sends $\Omega(k \log q)$ bits or Bob sends $\Omega(n \log q)$ bits. 

This gives $t_q = \Omega(\frac{\log q}{\log sw/n})$ lower bound. 

Highest possible lower bound from this technique $\Omega(\frac{\log |Q|w/n}{\log sw/n})$.

### Cell sampling 
[[Lower Bounds on Near Neighbor Search via Metric Expansion]]
$\newcommand{\bC}{\textbf{C}}$
Fix a $(s,t,w)$ DS. 
- sample a random set $\bC$ of $p \in (0,1)$ fraction of the cells. 
- prob that a fixed query $x$ can be answered by only probing $\bC$ is $\geq p^t$.  
- Expected # queries that can be answered correctly is $|Q|p^t$ by looking at $\bC$. 
- contradiction if $|w\cdot \bC| << n \cdot \log |Q|$ and $|Q|\cdot p^t \geq n$. 
>[!important] choice of $p$ setting $p = (\frac{n}{s})^2$.

This implies a bound of $t = \Omega(\frac{\log |Q|}{\log s/n})$.

- Nearest neighbour search
- works for non-deterministic data structures  as-well. 
The highest lower bound possible from this method is $\Omega(\frac{\log |Q|/n}{\log s/n})$. 😕?
---- 
... to be continued


# Part 2: Dynamic DS LBs 

Running example: Dynamic polynomial evaluation

Data: $p \in \mathbb{F}_q[x]$ of degree at most $n-1$. $q= poly(n)$. 
updates: updates coefficients
queries: $x \in \mathbb{F}_q$ output $p(x)$.

##### Chronogram [Fredman ,Saks 89]

A bunch of $n$ updates followed by a query:
$$U U U \ldots U Q$$
- divide the sequence into epochs.
- epoch $i$ has $\beta^i$ updates

Fix an epoch $i$, to learn information in epoch $i$, 
- cells that are not updated since the begining of epoch $i$ don't have information about updates in epoch $i$. 
- cells that are updated after epoch $i$ have too little information. 
- cells that are probed last probed in epoch $i$ := $C_i$ .  

>[!Note] Lemma: 
>for a random query, we must probe $\Omega(1)$ cells in expectation for every $i$. 

Lemma $\implies$ $t_q \geq \Omega(\log_\beta n) = \Omega(\frac{\log n}{\log (t_uw)})$.

Proof. Encoding argument.

$P$ is uniquely described by the update sequence.

 