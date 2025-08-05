# Introduction

^81fe0c

In a static data structure problem, we are given a domain $D$ of possible data, a domain $Q$ of possible queries, and a map $f: Q \times D \to A$, where $f(x, y)$ is the answer to query $x$ about data $y$.

>[!def] Static Data Structure Problem (Static DSP)
> A Static Data Structure Problem is given by the tuple $(D,Q,A,f)$ where
>-  $D$ is the domain of possible data, 
>- $Q$ is the domain of possible queries, 
>- $A$ is the set of possible answers  and 
>- $f: Q \times D \to A$ is a map where $f(x, y)$ is the answer to query $x$ about data $y$.
^920054

Typically the answer set $A = \{0,1\}$, unless specified explicitly the domain is assumed to be boolean values. We usually drop $A$ from the specification of the Static DSP.

A solution with parameters $s$, $b$, and $t$ is a method of storing any $y \in D$ as a data structure $\phi(y)$ in the memory of a random access machine, using $s$ memory cells, each containing $w$ bits, so that any query in $Q$ can be answered by accessing at most $t$ memory cells.

>[!def] Solution/ Scheme (s,w,t)
> A $(s,w,t)$ Solution to a Static Data Structure Problem $(D,Q,f)$ is given by the tuple $(s,t,\phi,\{Q_i\})$ where
> - $\phi: D \to [2^w]^s$ is an encoding map
> - $Q_i$ is a decision tree of depth at most $t$ for each query $i \in Q$. 

^873ea3


### Problems

>[!DSP] Dictionary Problem  
>- $D$ is the set of subsets $y\subseteq \{0, \dots , N-1\}$ of a certain size, 
>- $Q$ is the set $[0, ..., N-1]$, and
>- $f (x, y)=1$ if and only if $x \neq y$.

^89c656
[[Problems/Data_Structures/Static/Dictionary#^89c656]]



>[!DSP] Partial Match 
>- $D$ is the set of subsets $y \subseteq \{0,1\}^n$,
>- $Q$ is set of elements $x \in \{0, 1\}^n$
>- $f(x,y)$: $\exists z \in y \ \forall i \in [n]: x_i \leq z_i$. 

[[Problems/Data_Structures/Static/Partial Match]]


>[!DSP] Predecessor Problem 
>- $D$ = $2^U$ where $U = \{0, \dots 2^n-1\}$.
>- $Q$ = $U$.
>- $f(x,y)$ what is $\max\{z \in y | z \leq x\}$?

[[../DS Problems/Both/Predecessor]]


>[!DSP] Prefix Parity Problem 
>- $D$ is the set of subsets $y \subseteq U$.
>- $Q$ is set of elements $x\in U$.
>- $f(x,y)$: What is $|\{z \in y | z \leq x\}| \mod 2$?

[[DS Problems/Static/Prefix Parity]]


this problem reduces to Predecessor problem 

$\newcommand{\PAR}{\mathrm{PAR}}$
> [!CCP] Prefix Parity $(\PAR_{n,\ell})$ 
> **Alice's input:** $x \in U$.
> **Bob's input:** $y \subseteq U$ of size at most $\ell$.
> **Function:** determine $|\{z \in y| z \leq x\}| \mod 2$.


$\newcommand{\MEM}{\mathrm{MEM}}$
>[!CCP] Membership Problem $(\MEM_{N,\ell})$ 
>**Alice's input:** $x \in U = \{0, \dots N-1\}$
>**Bob's input:** $y \subseteq U$ of size at most $\ell$.
>**Function:** Decide if $x \in y$.
^7ac3b3


$\newcommand{\DISJ}{\mathrm{DISJ}}$
>[!CCP] Disjointness $\DISJ_{k,\ell}$ 
>**Alice's input:** $x \subseteq \{0, \dots , N-1\}$ of size $k$, 
> **Bob's input:** $y \subseteq \{0, \dots , N-1\}$ of size $l$, 
> **Function:** decide if $x \cap  y =\emptyset$.

^160eee
[[Problems/Communication_Complexity/SetDisjointness#^160eee]]


$\newcommand{\GT}{\mathrm{GT}}$
>[!CCP] Greater than $\GT_n$ 
>**Alice's input**: $x \in \{0,1\}^n$ 
>**Bob's input:** $y \in \{0,1\}^n$
>**Function:** Is $x \geq y$ ?
^19e2b1


$\newcommand{\Z}{\mathbb{Z}}$
>[!CCP] Span Problem #CCP
**Alice's input:**  $n$-dimensional vector $x \in \Z_2^n$  , and 
**Bob's input:** a subspace $y \in \Z_2^n$ (represented, e.g., by a basis of $kn$ vectors). 
**Function:** They must decide whether $x \in y$.
^20a241

They show that essentially no nontrivial protocol exists: in any randomized one-sided error $[a, b]$-protocol either $a=O(n)$ or $b=O(n^2)$.

>[!CCP] New Communication Problem $P_m(f)$ 
> **Alice's input:** gets $m$ strings $x_1 , \dots, x_m$ and 
> **Bob's input:** gets a string $y$ and an integer $1 \leq i \leq m$. 
> **Function:** Their aim is to compute $f(x_i , y)$.
^ab4de4

### Communication Complexity Prelims

>[!def] $[a,b]$-protocol
An $[a, b]$-protocol for $f$ is a protocol where the total number of bits that Alice sends Bob is at most $a$ and the total number of bits that Bob sends Alice is at most $b$. 
^d55d28


>[!def] $[t,a,b]^A$-protocol
A $[t, a, b]^A$-protocol for $f$ is a protocol where each of Alice's messages contains at most a bits and each of Bob's messages contains at most $b$ bits and at most $t$ messages are sent, with Alice sending the first message. A $[t, a, b]^B$ protocol is defined similarly.
^7fea2b

>[!def] Communication matrix 
Identify $f$ with the matrix $M$ with $M_{x, y}= f (x, y)$; i.e., index the rows by Alice's possible inputs, and the columns by Bob's possible inputs.


>[!def] Disecrepancy
>


- [ ] Define Discrepancy 
- [ ] Compute Discrepancy of a large mono chromatic rectangle  


- A Combinatorial rectangle  

# Communication Complexity vs Cell Probe Complexity

>[!lem] Lemma 1 [Mil94]
>If there is solution to the data structure problem with parameters $s, w,$ and $t$ then there is a $[2t, \lceil \log s \rceil, w]^A$-protocol for the communication problem.
^48662c

Lemma 2 proves a converse of lemma 1 in some sense. 
>[!lem] Lemma 2 
>If there is a $[O(1), a, b]$-protocol for the communication problem then the data structure problem has a solution with parameters $s=2^{O(a)}$, $t=O(1)$, and $b$.
^db8ec8

# Richness Technique


>[!def] $(u,v)$-richness
> We say that a matrix (and a problem) is $(u, v)$-rich if at least $v$ columns contain at least $u$ 1-entries.
^02c2c8


>[!lem] Lemma 5 Richness lemma 
>Let $f$ be a $(u, v)$-rich problem. If $f$ has a randomized one-sided error $[a, b]$-protocol, then $f$ contains a submatrix of dimensions at least $u/2^{a+2} \times v/2^{a+b+2}$ containing only 1-entries.
^09a188

### Disjointness lower bound

>[!lem] Theorem 11 Disjointness lower bound
> Let $k\leq \ell \leq N/2$. 
> If the disjointness problem $\DISJ_{k,\ell}$ has a deterministic $[a, b]$-protocol, then either $a=O(k)$ or $b=O(\ell)$. Moreover, for $a>k$, $b=O(\ell/2^{a/k} - a)$.
^b54aa6

***Proof of Theorem 11.*** 

- $\DISJ_{N,K,\ell}$ is $(\binom{N-\ell}{k},\binom{N}{\ell})$-rich. 
- By Lemma 5, we can find a 1-mono chromatic rectangle of size $\binom{N-\ell}{k}/2^a \times \binom{N}{\ell}/2^{a+b}$.
- Let the rows be $x_1, \dots, x_r$ and the columns be $y_1, \dots, y_s$. We have that $x_i \cap y_j = \emptyset$ $\forall i,j$.
- Let $x = \cup_i x_i$ and $y = \cup_j y_j$
So, we have 
- $\binom{|x|}{k} \leq \binom{N - \ell}{k}/2^a$ and $\binom{|y|}{\ell} \leq \binom{N}{\ell}/2^{a+b}$
-  $|x| + |y| \leq N$

---

>[!theorem] Theorem 12 SPAN
In any $[a, b]$ deterministic protocol for SPAN either $a=O(n)$ or $b=O(n^2)$.

^962676

***Proof of Theorem 12.***


What is the Property? 

- Richness and the some fixed approximation algorithm gives a large monochromatic rectangle. 

---
# Round Elimination technique

>[!lem] Round elimination lemma 
>Let $C=99$ and $R=4256$.  Suppose there is a randomized $[t, a, b]^A$-protocol for solving $P_{Ra}( f )$. Then there is a randomized $[t-1, Ca, Cb]^B$-protocol for solving $f$.


***Proof of Lemma 13.*** 

##### Prefix Parity

>[!theorem] Theorem 15. [MNSW'98]
>Let any $c>1$ be given. For a sufficiently large $n$, let $\ell=2^{\log^2 n}$, $a=\log^3 n$, $b=n^c$, $t= \sqrt{\log n}/10$. Then $PAR_{n,\ell}$ does not have a $[t, a, b]$-protocol.

***Proof of Theorem 15.*** 

$P^m(f)$ is the same as $P_m(f)$ but with the roles of Alice and Bob reversed. 

**Round elimination :** $PAR \to$ $P_m(f)$ or $P^m(f)$ 

**reduction:** $P_m(f)$ or $P^m(f)$ $\to PAR$ 
- A protocol for $PAR_{n,\ell}$ can be used as a protocol for $P_m(PAR_{n/m,\ell})$. 
- A communication protocol for $PAR_{n,\ell}$ can be used as a protocol for $P^m(PAR_{n - \log m -1, \ell/m})$. 

##### Range Query
- Prefix Parity $\to$ Range Query. 

##### Greater than

>[!theorem] Theorem 19. [MNSW'98]
>Let $C=99$. There does not exist a randomized $[k, n^{1/k}C^{-k}, n^{1/k}C^{-k}]$-protocol for $GT_n$.

^0ca5a1

- $[k, n^{1/k}C^{-k}, n^{1/k}C^{-k}]$-protocol for $GT_n$ $\implies$ $[k, n^{1/k}C^{-k}, n^{1/k}C^{-k}]$-protocol for $P_{n^{1/k}}(GT_{n'})$ for $n' = n^{k-1/k}$.  

Some sort of a self-reducibility property is used of the problem.  

###### Open Problem: [MNSW'98]
**Partial Match**
- No solution is known with the worst-case query time even polynomial in $n$ when the structure size is polynomial, and it has been conjectured that no such structure exists [Riv76].
- Yet not only does communication complexity fail to provide bounds better than $n \log s$,  but for this problem, we only know how to show a $\sqrt{\log n}$ lower bound when $s$ is polynomial in $m$, using the techniques of Section 4. 
- Getting bounds for this problem closer to $n \log s$ using communication complexity is an interesting open problem.

What is the Property here? 


Table of lower bounds


| Problem                                                   | Query time (t)                                          | Space(s)            | Cell size (w)  | parameters                      |
| --------------------------------------------------------- | ------------------------------------------------------- | ------------------- | -------------- | ------------------------------- |
| [[Problems/Data_Structures/Static/Dictionary\|Dictionary]]       |                                                         |                     |                |                                 |
| [[Problems/Data_Structures/Both/Predecessor\|Predecessor]]       | $\Omega(\sqrt{\log\log n})$ or $\Omega((\log m)^{1/3})$ | $(m \log n)^{O(1)}$ | $\log^{O(1)}n$ | $\|y\| = m$ , $y \subseteq [n]$ |
| [[Problems/Data_Structures/Static/Prefix Parity\|Prefix Parity]] | $\Omega(\sqrt{\log\log n})$ or $\Omega((\log m)^{1/3})$ | $(m \log n)^{O(1)}$ | $\log^{O(1)}n$ | $\|y\| = m$ $y \subseteq [n]$   |
| [[Problems/Communication_Complexity/Range Query\|Range Query]]            | $\Omega((\log m)^{1/3})$                                | $(m\log n)^{O(1)}$  | $\log^{O(1)}n$ |                                 |
|                                                           |                                                         |                     |                |                                 |
| [[Problems/Communication_Complexity/Membership\|Membership]]              |                                                         |                     |                |                                 |
| [[Problems/Communication_Complexity/Greater than\|Greater than]]          |                                                         |                     |                |                                 |
| [[Problems/Communication_Complexity/SetDisjointness\|SetDisjointness]]    |                                                         |                     |                |                                 |
| [[Problems/Communication_Complexity/Span\|Span]]                          |                                                         |                     |                |                                 |
