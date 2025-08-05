---
{"publish":true,"title":"Simulation beats richness new data-structure lower bounds","created":"2025-05-24T17:36:29.312+01:00","modified":"2025-07-11T13:23:18.426+01:00","published":"2025-07-11T13:23:18.426+01:00","cssclasses":""}
---


# Simulation beats richness new data-structure lower bounds

>[!meta]- Abstract
- We develop a new technique for proving lower bounds in the setting of asymmetric communication, a model that was introduced in the famous works of Miltersen (STOC’94) and Miltersen, Nisan, Safra and Wigderson (STOC’95). 
- At the core of our technique is the first simulation theorem in the asymmetric setting, where Alice gets a $p × n$ matrix x over $\mathbb F_2$ and Bob gets a vector $y \in \mathbb F_2^n$. 
	- Alice and Bob need to evaluate $f(x· y)$ for a Boolean function $f: \{0,1\}^p → \{0,1\}$. 
	- Our simulation theorems show that a deterministic/randomized communication protocol exists for this problem, with cost $C· n$ for Alice and $C$ for Bob, if and only if there exists a deterministic/randomized *parity decision tree* of cost $Θ(C)$ for evaluating $f$. 
- As applications of this technique, we obtain the following results: 
	1. The first strong lower-bounds against randomized data-structure schemes for the Vector-Matrix-Vector product problem over $\mathbb F_2$. Moreover, our method yields strong lower bounds even when the data-structure scheme has tiny advantage over random guessing. 
	2. The first lower bounds against randomized data-structures schemes for two natural Boolean variants of Orthogonal Vector Counting. 
	3. We construct an asymmetric communication problem and obtain a deterministic lower-bound for it which is provably better than any lower-bound that may be obtained by the classical Richness Method of Miltersen et al. (STOC ’95). 
	This seems to be the first known limitation of the Richness Method in the context of proving deterministic lower bounds.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/H2DR4X4Q)
> Authors:: [[people/Arkadev Chattopadhyay\|Arkadev Chattopadhyay]], [[people/Michal Koucký\|Michal Koucký]], [[people/Bruno Loff\|Bruno Loff]], [[people/Sagnik Mukhopadhyay\|Sagnik Mukhopadhyay]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/3188745.3188874
> doi:: 
> bibliography:: Chattopadhyay, Arkadev, Michal Koucký, Bruno Loff, and Sagnik Mukhopadhyay. 2018. ‘Simulation Beats Richness: New Data-Structure Lower Bounds’. In _Proceedings of the 50th Annual ACM SIGACT Symposium on Theory of Computing_, 1013–20. STOC 2018. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/3188745.3188874](https://doi.org/10.1145/3188745.3188874).


---
## Self Notes


Model:: Static Randomized lower bound 
Techniques:: [[Simulation]] Theorem for Asymmetric Communication, Parity Decision Trees
problems:: [[Problems/Data_Structures/Static/Vector-Matrix-Vector Product\|vector-Matrix-vector product]] over 𝔽₂, Boolean Variants of [[Problems/Data_Structures/Static/Orthogonal Vector Counting\|Orthogonal Vector Counting]], [[Problems/Data_Structures/Static/Orthogonal Gap Majority\|Orthogonal Gap Majority]]
lbs:: 
- ${\rm VMV}_{n \times n}$ : $t = \Omega(\frac{\epsilon n}{\log \frac{Sw}{n}})$ or error $\geq \frac{1}2 + 2^{-\epsilon n}$
- ${\rm OVC}_{n \times n}$ :  $t = \Omega(\frac{\epsilon n}{\log \frac{Sw}{n}})$ or error $\geq \frac23 + 2^{-\epsilon n}$
- ${\rm OGM}_{n \times n}$ : $t = \Omega(\frac{\epsilon n}{\log \frac{Sw}{n}})$ or error $\geq \epsilon$



## Reading notes



  



