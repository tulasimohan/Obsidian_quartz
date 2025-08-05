---
{"publish":true,"created":"2025-05-24T17:36:35.089+01:00","modified":"2025-05-24T17:36:31.157+01:00","published":"2025-05-24T17:36:31.157+01:00","cssclasses":""}
---

#talk
$\newcommand{\F}{\mathbb{F}}$

# Communication Complexity to prove DS lower bounds. 

## Miltersens's lowerbound
##### The Game
**Bob:** Datum
**Alice :** Query
**Goal:** Alice computes the answers to Alice's query on Bob's input. 
(Note that only Alice is expected to know the final answer.)
##### Protocol from Data Structure
- $t$ rounds
- Alice sends $\log s$ bits per round. 
- Bob sends $w$ bits per round. 
### Communication Complexity lower bounds

**Asymmetric Communication Lower bounds**
- $O(A,B)$ protocol is where Alice sends $A$  and Bob sends $B$ bits.
- $\Omega(A,B)$ lower bound says wither Alice sends $A$ bits or Bob sends $B$ bits to compute the function.  
- We only expect Alice to know the answer at the end of the computation. 

**Polynomial Evaluation** 
**Data:** Polynomials $P \in \F_p[x]$ of degree $\leq n-1$.The field size $(p = \theta(n^2)$).  
**Queries:** Given $x \in \F_p$, output $P(x)$.   

**Property:** 
The answers to any $n$ queries determines the data point(in this case polynomial). 

**Implications**
- $\exists$ $O(t\log s, t w)$ protocol from Data Structure
- If we have a $\Omega(A,B)$ lower bound for the same problem, then $t \log s \geq A$ or $tw \geq B$. 
  $$t \log s \geq \log p /4 \text{\ or\ } tw \geq n \log p$$
- Polynomial evaluation with parameters $(n,p)$ has a lower bound of $\Omega({\log p} /4, n \log p)$. 

$t = \Omega(\min \{\frac{\log p/4}{\log s}, \frac{n \log p}{w}\})$ 

##### Rectangle Argument
- Assume Alice sends $< \log p/4$ bits.
- Number of rows in the communication matrix = $p$,
- Number of columns in the communication matrix = $p^n$,
- There exists a rectangle which is at least $(p/2^{\log p/4}, p^n/2^B) = (p^{3/4},\frac{p^n}{2^B})$ large and each row is monochromatic. 
This means that there exist $p^n/2^B$ distinct polynomials which agree on a set of $p^{3/4}=n^3/2$ inputs. Which means $p^n/2^B \leq 1 \implies n\log p \leq B$. 

##### Limitations
- $\Omega(A,B)$ communication lower bound $\implies$ $t \geq \min\{\frac{A}{\log s},\frac{B}{w}\}$.
- There is protocol in which Alice and Bob send $O(\log n)$ bits for Polynomial evaluation.
- In general, any DS problem with $n^c$ queries bound never better than $t \geq c$.  

## Patrascu, Thorup 
##### The Game
**Alice:** $k$  queries i.e. $x_1, \dots, x_k \in \F_p$.
**Bob:** a polynomial $P$ of degree $\leq n$ over $\F_q$.

#### Data Structure $\implies$ protocol
- Bob builds data structure on input polynomial $P$.
-  Alice simulates the query algorithm on her inputs in parallel:  
	- For the cells needed at each step, Asks Bob for contents.
	- specifying a set of $k$ cells is cheaper than specifying each of the $k$ cells separately. 
	- $\binom{s}{k} = k \log {s/k}$ bits. 

- There is a $O(tk\log s/k,tkw)$ protocol for this game. 
- A $\Omega(A,B)$ protocol for this problem implies that $t \geq \min \{ \frac{A}{k \log s/k}, \frac{B}{kw}\}$. 

### Communication lower bound
- Assume Alice sends $< k\log p/4$ bits.
- Bob sends $B$ bits. 
- The communication matrix has $p\choose k$ rows and $p^n$ columns 
- There exists a rectangle with richness $(\binom{p}{k} / k\log (p/4) , p^n / 2^B)$

If there is a large rectangle with $\binom{p}{k} / k\log (p/4)$,
Let $U$ be the union of all the sets of the rows in the rectangle, let $|U|=X$. 
$\binom{X}{k} \geq \binom{p}{k}/k\log (p/4)$. 

$\implies (\frac{eX}{k})^k \geq (\frac{p}{k})^k$ $\cdot \frac{1}{k \log p/4}$ 

Choose $k = n\log p/2tw$. 

#### Trivial Protocols
**Alice:** sends $k \log p$ $\implies$ $k \leq n\log p/ tw \simeq n/t$
**Bob:** sends $n \log p$ $\implies$ if $k \leq n/t$, $t \geq \log p/\log (St/n)$.

this limits the approach from proving $\log p/ \log \log p$ lower bounds. 