by Oliver Korten, Tonian Pitassi, Russel Impagliazzo
$\newcommand{\NC}{\mathrm{NC}}$
$\newcommand{\zo}{\{0,1\}}$
## Abstract

In this work we observe a tight connection between three topics: 
- $\NC^0$ cryptography, 
- *$\NC^0$ range avoidance*, and 
- *static data structure lower bounds*. 
  
Using this connection, we leverage techniques from the cryptanalysis of NC0 PRGs to prove state-of-the-art results in the latter two subjects. 

>Our **main result** is a 
>- quadratic improvement to the best known static data structure lower bounds, 
breaking a barrier which has stood for several decades. 

Prior to our work, 
- the best known lower bound for any explicit problem with M inputs and N queries was 
$$S ≥ N^{\frac1t}  (\log M)^{1− \frac1t}$$ for any setting of the word length w (where S = space and t = time) [Sie89]. 
- We prove, for the same class of explicit problems considered in [Sie89], a quadratically stronger lower bound of the form $$S \geq \tilde{\Omega}(N^ \frac2t \cdot (\log M)^{1− \frac2t}  \cdot 2^{−O(w)})$$ for all even $t > 0$. 
- Second, for the restricted class of non-adaptive bit probe data structures, we improve on this lower bound polynomially: for all odd constants $t > 1$ we give an explicit problem with $N$ queries and $M ≤ N O(1)$ inputs and prove a lower bound $$S ≥ \Omega(N^{2/t +ϵ_t})$$ for some constant $ϵ,t > 0$. 
- Our results build off of an exciting body of work on refuting semi-random CSPs (e.g., [AGK21, GKM22, HKM23]). We then utilize our explicit cell probe lower bounds to obtain the best known unconditional algorithms for $\NC^0$ range avoidance: we can solve any instance with stretch $n \to m$ in polynomial time once $m >> n^{t/2}$ when $t$ is even; with the aid of an NP oracle we can solve any instance with $m > n^{t/2 − ϵ_t}$ for $ϵ_t > 0$ when $t$ is odd. Finally, using our main correspondence we establish novel barrier results for obtaining significant improvements to our cell probe lower bounds: 
	(i) near optimal space lower bounds for an explicit problem with $t = 4$, $w = 1$ implies $\rm{EXP}^{\rm{NP}} \not\subseteq \NC^1$ ; 
	(ii) under the widely-believed assumption that polynomial-stretch $\NC^0$ PRGs exist, there is no natural proof of a lower bound of the form $S ≥ N^{Ω(1)}$ when $t = ω(1)$, $w = 1$.
---

## Introduction
### Local PRGs

#### $\NC^0$ Pseudorandom Generators 

A prominent line of work initiated in [Gol00, CM01] has studied the existence of cryptographic PRGs in $\NC^0$ . 

>[!Def] $\NC^0_t$-PRG
>An $\NC^0_t$-PRG is function $G : \{0, 1\}^n → \{0, 1\}^m$, $m > n$, so that: 
>(1) each output depends on only $t$ inputs, and 
>(2) $G$ is a *cryptographic pseudorandom generator*: no polynomial time algorithm can distinguish a random output of $G$ from a truly random $m$ bit string. 
>
>We say that $G$ is an $\NC^0$ generator if it is $\NC^0_t$ for some $t = O(1)$. 
>

The existence of such PRGs has been the subject of a great deal of work over the past two decades; 
we refer the reader to a comprehensive survey [App16] and the references therein. 
An important parameter is the stretch of the generator, which denotes the relation between $n$, $m$. We say that $G$ has nontrivial stretch if $m > n$, and polynomial stretch if $m ≥ n^{1+Ω(1)}$. 

>$\NC^0$ generators with nontrivial stretch can be shown to exist under standard number theoretic cryptographic assumptions [AIK06], 

however their utility has so far been limited. 

On the other hand,
>$\NC^0$ generators with polynomial stretch are not known to exist under any more standard hardness assumptions, 

but have been found to have a wide range of advanced cryptographic applications [IKOS08], most notably in the construction of Indistinguishability Obfuscation [JLS21, JLS22]. 

For this reason, a great deal of work has gone into studying the existence of polynomial stretch $\NC^0$ PRGs as a foundational assumption in its own right, and various algorithmic methods for distinguishing such PRGs have been studied. The current state of the art shows that an $\NC^0_t$ generator $G : \{0, 1\}^n → \{0, 1\}^m$ can be broken in polynomial time once $m >> n^{t/2}$ ([MST03, AOW15, AGK21]).

---

### $\NC^0$ range avoidance
>[!Def] Range Avoidance Problem
**Input:** an $\NC^0_t$ generator $G : \{0, 1\}^n → \{0, 1\}^m$ with $m > n$ and $t = O(1)$.
**Output:** output a string $y \in \{0, 1\}^m$ such that $y \not\in \rm{range}(G)$.

- The range avoidance problem (for general $G : \{0, 1\}^n → \{0, 1\}^m$ computed by polynomial size circuits) was introduced in [KKMP21], and shown in [Kor21] to be intimately connected to de-randomization and to the problem of proving circuit lower bounds for exponential time classes.
- $\rm{P}^{\rm{NP}}$ algorithm for Range avoidance for $\NC^0$ circuits $\implies$ $\rm{EXP}^{\rm{NP}} \notin \NC^1$. 
- Unconditional algorithms for Range avoidance are known for stretch $m >> \frac{n^{t-1}}{\log n}$. 
- **Open Question:** Is there an unconditional $\rm{P}^{\rm{NP}}$ algorithm for $\NC^0$ range avoidance for general polynomial stretch? 

---
### The Main Correspondence

- bit probe model

>[!Obs] Observation 1
>Let $F : [N] × [M ] → \{0, 1\}$ be a data structure problem, which we interpret as a matrix $F \in \{0, 1\}^{N×M}$ with $N$ rows and $M$ columns below.
>The following are equivalent:  
>1. $F$ has does not have nonadaptive bit probe data structures with space complexity $S$ and time complexity $t$.  
>2. The columns of $F$ are a set of $M$ strings $F \subseteq \{0, 1\}^N$ , $|F| = M$ , such that for any $\NC^0_t$  generator $G : \{0, 1\}^S → \{0, 1\}^N$ , there exists a string $f \in F$ with $f \notin \rm{range}(G)$.

---
## Results

- Columns support a $k$-wise independent distribution. 
>[!Thm] Theorem 1. 
>Let $F : [N ] × [M ] → \{0, 1\}$ be a data structure problem such that there exists a $k$-wise independent distribution supported on its columns. Let $S, t, w \in N$ be given with $t$ an even number and assume $k > tw + 1$. Then, for any space $S$, time $t$, word length $w$ cell probe data structure solving $F$ we must have:  
>1. $S ≥ (\frac{N} {\log N})^ {2/t}· (\frac{k}{\log N})^ {1− 2 /t} ·t^{−1} \cdot 2^{−O(w)}$ for all $t \log N ≤ k ≤ N 2^{−O(tw)}t^{−t/2}$  
>2. $S ≥ (\frac{N} {\log N})^ {\frac{1}{t(1/2 + 2/k)}} ·t^{−1} \cdot 2^{−O(w)}$ for all $tw + 1 ≤ k ≤ t \log N$

- Theorem 1 can be strengthened to $\gamma$ almost $k$-wise independent distributions.  

- [ ] **Question:** The quadratic improvement that they prove using their methods, can it be done using the existing machinery? 

---
$\newcommand{\calC}{\mathcal{C}}$
### Definitions and concepts

- **$t$-XOR scheme:** $\calC = (X,V,c)$
- $X$: index set, $V:$ variables, $c:X \to \binom{V}{t}$ mapping 

Given $f: X \to \{ -1, +1 \}$, define 

- $Val(\calC, f,R)$:= $|\E_{x \in X} f_x \prod_{i \in c_x} R(i)|$

- $OPT(\calC,f)$:= $\max_{R \in \{+1,-1\}^V} Val(\calC, f ,R)$

- [ ] what is the motivation behind these definitions? 

the name XOR scheme comes from MAX-t- XOR CSPs. 

---
### Theorems
$\newcommand{\F}{\mathbb{F}}$
##### Section 1 Introduction 
Theorems about Lb from $k$-wise independence 
- **Theorem 1** gives lower-bound on the space for tables which support $k$-wise independent distributions on its columns. 
- **Theorem 2** is similar to theorem 1 for $\gamma$-almost $k$-wise independent distributions.
---
Theorems about range avoidance
- **Theorem 3** says $\exists$ a list of strings computable in poly-time which misses all $\NC^0_t$ generators $G:\{0,1\}^n \to \{0,1\}^m$ for some choice of $m$.
- **Theorem 4** : for every $t$ locally computable generator, it gives a string which not only is in the range, but differs from all the strings in range on at least $\frac12 -\epsilon$ fraction of input locations.
---
Theorems about implications of their lower bounds
- **Theorem 5**: Explicit bit probe lower bounds $\implies$ lower bounds like $EXP^{NP} \not\subseteq NC^1$ etc. based on the number of data points. 
- **Theorem 6**: Natural proof barriers for Bit Probe Lower Bounds. 
##### Section 3 Cell Probe lower bounds via CSP- Pseudorandomness
- **Theorem 7**: for any locally-computable generator over output space $\{±1\}^N$ , we can associate a small collection of XOR schemes indexed by $[N]$ (or by large subsets $X ⊆ [N ])$, so that for any $f \in range(G)$, we have that $OPT(\calC, f )$ is large for one of the schemes $\calC$ in our collection. 
- **Theorem 8** : XOR schemes and Permutation ensembles. 
- **Theorem 9**: Tail bound, permutation ensemble. 
- **Theorem 10**: Tail bound on $OPT(\calC,f)$ for a $\gamma$ almost $k$ wise independent $f$.  
- **Theorem 11**: Matrix Bernstein
- **Theorem 12**:DS space lower bound $\chi-\F-Eval^d$ where $\chi: \F \to \{0,1\}$ is an arbitrary balanced function. 
- **Theorem 13**: DS space lb for $\F_2-Eval_n^d$ problem.
##### Section 4 Beating the limited independence bound
- **Theorem 14**:  about $\NC^0_t$ generator and XOR schemes.
- **Theorem 15**: Multi-hyper graph, symmetric difference operator. 
- **Theorem 16**: $t$- XOR scheme and upper bound on $\Pr[OPT(\calC,\bf{f})]$ for a random $\bf{f}$.  

##### Section 5 Algorithmic implication of our lower bounds
- **Theorem 17**: Correlation variant of Theorem 7. 

##### Section 6 Towards Stronger Lower Bounds

##### Appendix 
- **Theorem 18**: Kikuchi method. 


- [ ] **Question:** Why $\NC^0$? What is the connection with Data Structures and $\NC^0$?


- [ ] Read Section 6 of the paper. 

### 6 Towards stronger lower bounds

**Goal 1**: Strong lower bounds 
$S = \Omega(n^\epsilon)$ for Non-adaptive $t = O(1)$ bit probe queries.

**Goal 2**: Super strong lower bounds
$S = \Omega(n - n^{o(1)})$ for DS making 4 non-adaptive bit probe queries. 

No. of data points $M$ is a function of number of queries $N$.
$poly(N) \leq M(N) \leq exp(N^{o(1)})$ 

**Explicit**: Sequence of strings $(x_n)_{n \in \mathbb{N}}$ is *explicit*. 

#### 6.1 Consequences of Explicit Bit Probe Lower Bounds


#### 6.2 Natural Bit Probe Lower Bounds break $\NC^0$ PRGs

>[!Def] Definition 13 (Natural Bit Probe Lower Bounds). 
>A $(N, M, S, t)$ natural property is an algorithm $A$ which takes as input the description of a data structure problem $F : [N ] × [M ] \to \{0, 1\}$, and outputs a value in {Hard, ?}, such that:  
>1. If $A(F) =$ Hard, then $F$ requires space $≥ S$ or time $> t$ for nonadaptive bit probe data structures.  
>2. If $F$ is chosen uniformly at random amongst all functions $[N ] × [M ] → {0, 1}$, then with probability at least $(N M)^{−O(1)}$, $A(F) =$ Hard.


In our discussion we will have $N$ as our main asymptotic complexity parameter, $t$ fixed, and $S = S(N)$, $M = M (N)$ growing as a function of $N$.

**$(N,M(N),S(N),t)$ - natural property** := A natural proof of a space lower bound of $\Omega(S(N))$ for a $t$ - data strucutre with $M(N)$ data points. 
**$k$ size computable**: computable by a circuit of size $k$. 

**A cryptopgraphic PRG $G:\{0,1\}^n \to \{0,1\}^m$ has hardness $\lambda$**:
if of size $\leq \lambda$ circuits fail to distinguish the $G$ with advantange $\leq \lambda^{-1}$. 


>[!Lem] Lemma 9. 
>Say that $G : \{0, 1\}^S \to \{0, 1\}^N$ is a cryptographic $NC^0_t$ PRG with hardness $λ$. Then there does not exist an $(N, M, S, t)$ natural property computable by circuits of size $k$ unless $λ ≤ k · poly(N, M)$.

- $G$ is an $NC^0_t$ PRG with hardness $\lambda$ $\implies$ $\not\exists$ $(N,M,S,T)$ natural property computable by circuits of size $k$ unless $\lambda \leq k \cdot poly(N,M)$. 
  
- **Contrapositive:** If $\exists (N,M,S,T)$ natural property computable by circuits of size $k$ $\implies$ $\NC^0_t$ PRGs are not $\lambda$ hard for $\lambda \geq k \cdot poly(N,M)$.

$M$ = no. of data points
$N$ = no. of queries 

**Proof:** Let $G$ be a cryptographic $NC^0_t$ PRG with hardness $\lambda$. 
Consider $G^{\otimes M}: \{0,1\}^{SM} \to \{0,1\}^{MN}$ given by $G(E_1,\dots ,E_m) = (G(E_1),\dots, G(E_M)$. 
by Hybrid argument $G^{\otimes M}$ is $\lambda/M$ hard. 


- $(N,M,S,t)$ definitions is about non-adaptive DS.


>[!Lem] Lemma 10.
>If there exists an $NC^0$ PRG $G:\{0,1\}^n \to \{0,1\}^m$ with arbitrary polynomial strech($m \geq n^{1+ \Omega(1)}$) and hardness $\lambda$, then for every $c \in \mathbb{N}$ there exists an $NC^0$ PRG $G':\{0,1\}^n \to \{0,1\}^{n^c}$  with hardness $\geq n^{-O(1)}\lambda$.  


>[!Lem] Lemma 11 [AIK'06] Applebaum, Ishai, Kushilevitz
>If there exists an $NC^1$ PRG with hardness $\lambda$, then there exists an $NC^0_4$ PRG 
> $G':\zo^m \to \zo^{m + m^{.99}}$ for some $m \leq poly(n)$ with hardness $\geq n^{-O(1)}\lambda$.



#### 6.3 Approaches to strong lower bounds via Communication Complexity
