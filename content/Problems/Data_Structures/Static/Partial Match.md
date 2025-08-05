---
{"publish":true,"created":"2025-05-24T17:36:33.154+01:00","modified":"2025-07-07T13:06:08.195+01:00","published":"2025-07-07T13:06:08.195+01:00","cssclasses":""}
---

# Partial Match

>[!DSP] Partial Match
>**Data:** Given a database of $n$ points in $\{0,1\}^d$, the partial match problem is: 
>**Query:** For $x \in \{0, 1, *\}^d$, find a database point $y$ such that for every $i$ whenever $x_i \neq *$, we have $x_i = y_i$. 

[[Patrascu Unifying the landscape.canvas|Patrascu Unifying the landscape]] obtains current best non-trivial LB.

The best previous bound [[Cell-probe lower bounds for the partial match problem\|Jayram, Khot, Kumar, Rabani '03]] for Alice’s communication was $\Omega(d/ \log n)$ bits, instead of our optimal $\Omega(d)$.

**Prior work:**
- [[Lower bounds for high dimensional nearest neighbor search and related problems\|Lower bounds for high dimensional nearest neighbor search and related problems]] by Bordoin, Ostrovsky, Rabani 1999
- [[Cell-probe lower bounds for the partial match problem\|Cell-probe lower bounds for the partial match problem]] by Jayram, Khot, Kumar, Rabani 2003 
- [[Resources/Notes/Miltersen, Nisan, Safra, Wigderson\|Miltersen, Nisan, Safra, Wigderson]] 1998
- [[Higher lower bounds for near-neighbor and further rich problems]] by Patrascu, Thorup 2006 


##### Communication Game

>[!Tip] Theorem 1.1. [Citation?]
>Let Alice hold a string in $\{0, 1,*\}^d$, and let Bob hold $n$ points in $\{0, 1\}^d$. In any bounded-error protocol answering the partial match problem, either Alice sends $\Omega(d)$ bits or Bob sends $\Omega(n^{1−\epsilon})$ bits, for any constant $\epsilon > 0$.

By the standard relation between asymmetric communication complexity and cell-probe data structures [[Resources/Notes/Miltersen, Nisan, Safra, Wigderson\|MNSW'98]]
and decision trees [[Hardness of Nearest Neighbor under L-infinity\|Andoni, Croitoru, Patrascu '08]], this bounds implies that 
- a data structure for the partial match problem with cell-probe complexity $t$ must use space $2^{\Omega(d/t)}$, assuming the word size is $O(n^{1−\epsilon}/t)$; 
- a decision tree for the partial match problem must have size $2^{\Omega(d)}$, assuming the depth is $O(n^{1−2\epsilon}/d)$ and the predicate size is O($n^\epsilon$).
