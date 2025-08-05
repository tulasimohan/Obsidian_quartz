---
{"publish":true,"title":"Approximating Nash Equilibria and Dense Bipartite Subgraphs via an Approximate Version of Caratheodory's Theorem","created":"2025-05-24T17:36:33.828+01:00","modified":"2025-06-16T00:27:28.210+01:00","published":"2025-06-16T00:27:28.210+01:00","cssclasses":""}
---


>[!meta] Abstract
We present algorithmic applications of an approximate version of Caratheodory's theorem. The theorem states that given a set of vectors X in Rd, for every vector in the convex hull of X there exists an ε-close (under the p-norm distance, for 2 ≤ p &lt; ∞) vector that can be expressed as a convex combination of at most b vectors of X, where the bound b depends on ε and the norm p and is independent of the dimension d. This theorem can be derived by instantiating Maurey's lemma, early references to which can be found in the work of Pisier (1981) and Carl (1985). However, in this paper we present a self-contained proof of this result.Using this theorem we establish that in a bimatrix game with n x n payoff matrices A, B, if the number of non-zero entries in any column of A+B is at most s then an ε-Nash equilibrium of the game can be computed in time nO(log s/ε2}). This, in particular, gives us a polynomial-time approximation scheme for Nash equilibrium in games with fixed column sparsity s. Moreover, for arbitrary bimatrix games---since s can be at most n---the running time of our algorithm matches the best-known upper bound, which was obtained by Lipton, Markakis, and Mehta (2003).The approximate Carathéodory's theorem also leads to an additive approximation algorithm for the densest k-bipartite subgraph problem. Given a graph with n vertices and maximum degree d, the developed algorithm determines a k x k bipartite subgraph with density within ε (in the additive sense) of the optimal density in time nO(log d/ε2).

> [!meta] Metadata
> zotero_link:: [Accepted Version](zotero://select/groups/5902932/items/I2IDKNZS)
> Authors:: [[people/Siddharth Barman\|Siddharth Barman]], 
> Related:: 
> url:: https://doi.org/10.1145/2746539.2746566
> doi:: 
> bibliography:: Barman, Siddharth. 2015. ‘Approximating Nash Equilibria and Dense Bipartite Subgraphs via an Approximate Version of Caratheodory’s Theorem’. In _Proceedings of the Forty-Seventh Annual ACM Symposium on Theory of Computing_, 361–69. STOC ’15. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/2746539.2746566](https://doi.org/10.1145/2746539.2746566).


---
# Self Notes


$\newcommand{\R}{\mathbb{R}}$
$\newcommand{\E}{\mathbb{E}}$
$\newcommand{\abs}[1]{\left||#1\right||}$


---

>[!Thm] Theorem 8. 
>Let $G$ be a graph with $n$ vertices and maximum degree $d$. Then, an ε-additive approximation of NDkS over $G$ can be determined in time  $n^{O( \log d/\epsilon^2)}$ .



> [!Thm] Caratheodory's theorem
> Given a set of vectors $X$ in $\R^d$, every vector in the convex hull of $X$ can be expressed as a convex combination of at most $d+1$ vectors in $X$. 


> [!Thm] Approximate Catheodory's theorem 
> Given 
> - a set of vectors $X$ in $\R^d$, 
> - for every vector in the convex hull of $X$ 
>
>there exists 
> - an $\epsilon$-close vector (under the $p$-norm distance, for 2 ≤ p < ∞)
> 
> that can be expressed as a convex combination of at most $b$ vectors of $X$, 
> where the bound $b$ depends on $\epsilon$ and the norm $p$ and is independent of the dimension $d$.

***Proof*.** 
Let $\mu$ be any point in the convex hull of $X$. By Caratheodory's theorem, there exist $\mu$ can be approximated by a convex combination of $d+1$ points from $X$.  

- Sample $b$ vectors from the distribution given by the convex combination. 
- In expectation the sum of the samples will be the same as $\mu$. 
- Use Khintchine's inequality to show that the sample average is indeed close to $\mu$ w.h.p. 
--- 
>[!Lemma]  Khintchine inequality
>- Let $r_1, r_2, \dots , r_m$ be a sequence of i.i.d. Rademacher $±1$  random variables, i.e., $\Pr(r_i = ±1) = 1/2$ for all $i \in [m]$. 
>- In addition, let $u_1, u_2, \dots, u_m \in R^d$ be a  deterministic sequence of vectors. Then, for $2 \leq  p < \infty$
 
 $$\E_{r}\left[\abs{\sum_i r_i u_i}_p\right] \leq \sqrt{p} \cdot (\sum_i \abs{u_i}_p^2)^{\frac12}$$
Proof of Khintchine's inequality: out of scope

 ---
> [!problem] Densest $k$-subgraph problem [[NDkS]]
> Given 
> - a graph with $n$ vertices and 
> - maximum degree $d$, 
>
>determine 
>a subgraph with exactly $k$ vertices with normalized density within $\epsilon$ (in the additive sense). 
> 

- [Alon, Arora, Manokaran, Moshkovitz, Weinstein '11](http://www.tau.ac.il/~nogaa/PDFS/dks8.pdf) : Inapproximability of densest κ-subgraph from average case hardness. 

>[!Problem] Densest $k$ Bipartite Subgraph [[DkBS]] 
>- Variant of NDkS
>- Find size-$k$ vertex subsets $S,T$ of maximum density. 
>- In the bipartite case, density of vertex subsets $S$ and $T$ is defined to be the  number of edges between the two subsets divided by $|S||T|$.



>[!Corollary]
>Approximate Caratheodory’s theorem $\implies$ additive approximation algorithm for the normalized densest k-subgraph problem

### Proof idea: 

- Formulate a bilinear/quadratic program in which 
	- the objective matrix is column sparse.  
	- the feasible region is contained in a simplex. 
We use this observation to develop an additive approximations for NDkS  and DkBS.

Given a 
- simple graph $G = (V,E)$, and 
- size parameter $k \leq |V|$. 
**Goal:** maximum density subgraph containing $k$ vertices. 



# Reading notes



  
_Imported: 2025-03-10 16:01_

### Upper and Lowerbounds

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The approximate Carath ́eodory’s theorem also leads to an additive approximation algorithm for the normalized densest k-subgraph problem >  



