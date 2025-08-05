---
{"publish":true,"title":"Adapt or Die","created":"2025-05-24T17:36:36.555+01:00","modified":"2025-07-07T13:05:17.608+01:00","published":"2025-07-07T13:05:17.608+01:00","cssclasses":""}
---


## Introduction

[@BrodyL15] have shown Dynamic Data Structure lower bounds in the two restricted settings of Non-adaptive Queries and Memory-less Updates defined below. We show that these two lower bound proofs from this paper are natural.  

## Non-adaptive query lower bound for Indexing

> [!note] Non-adaptive queries
> The memory location probed by a query is pre-determined by the query function.

> [!note] Indexing problem
> - **Data**: $\{(S_1,\dots,S_k,j): j \in [n],\ S_i \in \{0,1\}^n \ \forall i \in [k]\}$  
> - **Queries**: $\forall i \in [k]$, $q_i$ outputs $j^{\text{th}}$ bit of $S_i$,  
> - **Updates**: $\forall j \in [n]$, updates the index part of the data to $j$,  
> - **Skeleton**:  
>   The table consists of $k2^n$ rows and $k$ columns.   
>   The graph induced by the updates on the rows of the table is that of $k2^n$ disjoint $n$-cliques.

> [!tip] Theorem [@BrodyL15]
> Any Non-adaptive Dynamic Data structure for the Indexing problem must have $t_q = \Omega (n/w)$ or $t_u = \Omega (k/w)$.

### Lower bound

Suppose Indexing has a non-adaptive data structure with query time $t_q$ and update time $t_u$.  

The lower bound proceeds by giving an encoding of $k$-random strings of $n$ bits each.  

Let $(X_1, \dots ,X_k)$ be $k$ $n$-bit strings.  

For each $j \in [k]$, run the non-adaptive query algorithm $q_j$ on $(X_1,\dots,X_k,1)$   
let $E_1$ be the string obtained by concatenating the answers to probes in the order they are probed. $|E_1| = k \cdot t_q$ (assuming word length $w=1$ in the encoding)  

For each update $i \in [n]$, run the update algorithm $u_i$ on $(X_1,\dots,X_k,1)$, let $E_2$ be the string obtained by concatenating the entries of the locations probed in the order they were probed.  
$|E_2| = n \cdot t_u$ (assuming word length $w=1$ in the encoding).  

Therefore, using $kt_q+nt_u$ bits, we can simulate all the updates and queries on $(X_1, \dots,X_k,1)$.   
Simulating update $i$ followed by query $j$ gives us $X_{i,j}$.   
Since $kt_q+nt_u$ bits encode $k$ binary strings of length $n$, $kt_q+ nt_u \geq nk$ and hence $t_q \geq n$ or $t_u \geq k$.   

---
## Memoryless Update Lower bound for Disjointness

- [ ] add this from miro notes

> [!note] Memoryless updates
> To begin with, the update function is non-adaptive, i.e., the memory locations to be updated are pre-determined by the update function. Furthermore, the update to the probed location is determined by the content of that location and not on the contents of other locations probed.

> [!note] Set-Disjointness
> - **Data**: $\{(S,T): S,T \subseteq [n]\}$  
> - **Queries**: Is $S\cap T = \varnothing$?  
> - **Updates**: $\forall i \in [n]$, add/remove $i$ to $T$.  
> - **Skeleton**:

#### Property 1 #property_DP1

We abstract out a property of the table of Indexing which is used to prove the lower bound.  

Consider the random variable $N(R)$, which is the $n \times k$ array obtained from the update neighbors of a random row $R$ of the table.  

This gives a distribution on the string of length $kn$.  
#property_DP1  
$H(N(R)))$ being large is the "Property" used to prove the above lower bound.  

If $H(N(R)) = h$, we get lower bounds of $t_q \geq h/k$ and $t_u \geq h/n$.  

##### Largeness

We now argue that a random table with the same skeleton as that of Indexing has #property_DP1.  

Brody and Larsen give an encoding of a random $S \subseteq [n]$ using $O(t_u \cot w)$ bits using any given memory-less data structure for Set-Disjointness.  
Encoding:
