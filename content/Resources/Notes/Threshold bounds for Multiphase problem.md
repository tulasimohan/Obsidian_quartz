by [[people/Raphael Clifford\|Raphael Clifford]], [[people/Allan Grønlund\|Allan Grønlund]], [[../people/Kasper Green Larsen\|Kasper Green Larsen]]

# Update time is large if the Query time is small


It is usually phrased as 
>[!Def] Patrascu's Multiphase problem
>**Phase I:** Receive $k$ subsets $X_1, \dots , X_k$ of a universe $[n]$ to preprocess.
>**Phase II:** We receive another set $Y \subseteq [n]$ and we are allowed to update the pre-processed memory.
>**Phase III:** We receive an index $i \in [k]$ and the goal is to return if $X \cap Y = \emptyset$. 

In our language it can be rephrased as
>[!Def] Multiphase Problem
> **Data:** $(X_1, \dots , X_k,Y)$ such that $X_i \subseteq [n]$ $\forall i \in [k]$ and $Y \subseteq [n]$. 
> **Updates:** $Y_{new} \subseteq [n]$ to update the $Y$ part in the data. 
> **Queries:** $\forall i \in [k]$, the query $q_i$ checks if $X_i \cap Y$ is empty.


>[!tip] Theorem
> Any cell probe data structure for the Multiphase problem on $k$ sets from a universe $[n]$, where $w^4 \leq  n \leq k$, using $kn^{O(1)}$ cells of $w = \Omega(\log k)$ space answering queries in $t_q = o(\log k/\log n)$ probes must have $t_u = \Omega(k^{1- o(1)}/w)$.  

**parameters:** Choosing  $n = \log k$, we get 
$s = k n^{O(1)}$ and $t_q = o(\log k/\log n) \implies t_u = k^{1-o(1)}/w$
$s = k \log^{O(1)} k$ and $t_q = o(\log k/\log \log k) \implies t_u= k^{1- o(1)}/w$. 

>[!Def] Lopsided Set Disjointness (LSD)
Universe $U$. 
Alice gets set $V$ of size $N$ such that $NB = |U|$ for some $B >1$. 
Bob gets $W \subseteq U$. 
Goal is to check if $V \cap W = \emptyset$?
 
>[!Def] Blocked LSD
Bob get an arbitrary subset $W$ of $[N] \times [B]$ 
Alice gets a subset $V \subset [N] \times [B]$ such that $\forall i \in [N]$, there exists a unique $b_i \in [B]$ such that $(i,b_i) \in V$.
Goal is check if $V \cap W = \emptyset$?

>[!tip] Theorem [Patrascu]
>In any deterministic protocol for Blocked-LSD, either Alice sends $\delta N \log B$ bits or Bob sends $NB^{1 - O(
>\delta)}$ bits. [[Blocked LSD lower bound]]

## Reduction from Blocked LSD to Multiphase problem

$N = n/\ell = \sqrt{\log k}\frac{n}{\sqrt{\log n}}$, $B = \sqrt{\log n}\frac{k}{\sqrt{\log k}}$

$n = \ell N$
k = $B/\ell$

$\ell = \sqrt{\log k/\log n}$, $w^4 < n <k$.

 
Given an instance of Block Lopsided Set Disjointness (Block LSD) i.e.  Bob gets $X \in [n/\ell]\times [k\ell]$,  Alice gets $Y \subseteq   [n/\ell] \times [k \ell]$ where $\forall i \in [k\ell]$ $\exists$ a unique  $b_i \in [n/\ell]$  such that $(i,b_i) \in Y$ 

Partition the inputs into $k$ disjoint blocks of $[\ell] \times [n/\ell]$ namely $X_1, X_2, \dots , X_k$ and $Y_1,\dots, Y_k$. 
Given a cell probe data structure for the Multiphase problem, Here is how the protocol for Blocked LSD proceeds. 

***Step 1:*** Bob preprocesses the memory with $Y_1, \dots , Y_k$ using $S = k n^{O(1)}$ memory cells. 

***Step 2:*** For each subset $X \subseteq [n]$ of size $\ell$, Alice simulates the updates the update $Y$ while maintaining a set of C(Y_1, \dots , Y_k, X) of memory locations probed and their contents. This is at most $k^{O(1)}t_u w$ bits in total since $\ell = \log k/\log n$. 

***Step 3:*** Alice simulates the query algorithm for the $i$th query on the input $(Y_1, \dots, Y_k, X_i)$ for each $i \in [k]$ in parallel. 
- For $t = 1 , \dots , t_q$, Alice simulates the $t^{th}$ step of the query algorithm let $c_{t,i}$ be be the cell probed by the query algorithm $i$ on the input $(Y_1, \dots Y_k,X_i)$ in the $t^{th}$ step. 
- If $c_{t,i} \in C(Y_1, \dots ,Y_k,X_i)$, then Alice knows the updated value of $c_{t,i}$ and she can look up the value, otherwise she adds the address of $c_{t,i}$ to $Z_t$ The cells added to $Z_t$ hold the same value since preprocessing, so she can ask for the value of it.    

$t_q k \log (s/k) \geq k\ell (n/\ell)^{1- \delta}$ or 
### Communicating a subset 

>[!tip] Lemma 1
>Consider a communication game where Bob receives a set $B \subseteq [2^w]$ of size $S$ and Alice receives a subset $A \subseteq B$ of size $k$. There is a deterministic protocol in which Alice sends $O(k \log S/k)$ bits and Bob sends $O(kw)$ bits, and after communicating Bob knows Alice's set.
>

$B \subseteq [2^w]$, $|B| = S$ $A \subseteq B$, $|A| = k$

Consider the hash function $h_a= \lfloor(ax \mod 2^w)/2^{w-M}\rfloor$ by Dietzfelbinger et al.
where $a$ is uniform odd integer less than $2^w$. 
