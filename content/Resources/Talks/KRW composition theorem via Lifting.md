a talk by OR Meir

- Depth of a circuit $C(f)$.
- $P$ vs  $NC'$ question. 
- State of the art $D(ANDREEV) \geq (3 - o(1))\log n$ [Hastad 93, Tal 14]
- Shrinkage technique: cannot prove better lb than 3  

[Karchmer- Raz-Wigderson-91]

Block composition

- $f:\{0,1\}^m \to \{0,1\}$ and $g:\{0,1\}^n \to \{0,1\}$

- $(f \diamond g)(X)$ where $X \in \{0,1\}^{m \times n}$
$X$ is an $m \times n$ matrix.  


>[!Conjecture] KRW conjecture 91
>$\forall f,g$: $D(f \diamond g) \approx D(f) + D(g)$ 

>KW relation: 
$D(f) = CC (KW_f)$

$KW_{f \diamond g} \approx KW_f \diamond KW_g$

$X \quad a=g(X)$    $b=g(Y) \quad Y$


### The Universal relation

-  $CC(U) \geq n$

- $U \diamond U$ [Edomonds, Impagliazzo, Rudich, S'gall 91] 
[Hastad, Widgerson 93]
Q: How do you define $U \diamond U$?

- $KW_f \diamond U$ for every $f$ [Gavinsky, Meir, Weisnstein, Wigderson 14]
[Koroth, Meir 18]

- The composition for $KW_f \diamond KW_{\oplus}$ [Hastad 93, Dinur,Meir 16]

- $KW_f \diamond KW_g$ for every $f$ and for every $g$ with tight adversary bound [Filmus, Meir , Tal 20]

- The composition $U \diamond KW_g$ for some maximally hard g. [Mihajin, Smal 20]

Adversary bound: from Quantum Query complexity,(generalization of Krapchenko bound).  


## Monotone Composition 

Monotone $KW$ relation $mKW$

Monotone NC seperations using KW relations. 
- STConnectivity [KW88]
- Clique[HG91, RW92]
- Matching [RW 92]
Used to seperation NC hierarchy using the Generation function [RM 97]

### Lifting 
[RM 97, SZ 09, S11, GP 14, GPW 15, GJ16, GLMWZ16, RNV16, RPRC16, CKLM18, GGKS18, HHL18]

- $S \diamond Gad$ where 
	- $S$ is a search problem from $\{0,1\}^k$ to some range $\mathcal{O}$.
	- Gad: $\{0,1\}^b \times \{0,1\}^b \to \{0,1\}$. 

- A recipie for showing monotone KW relations
	- Reducing a lifted problem $S \diamond Gad$ to KW relation. 
	- Using lifting theorem to prove a lower bound on $CC(S\diamond Gad)$. 

- Two such lifting theorems by Meir:
	- Lifting from query complexity [Chattopadhyay, Filmus, Meir, Pitassi 19] following [RM97, CKLM17, WYY 17]
	- Lifting from Nullstellensatz degree 
		[de Rezende, Meir, Pitassi, Robere, Vinyals 19]
## Semi-monotone Composition
