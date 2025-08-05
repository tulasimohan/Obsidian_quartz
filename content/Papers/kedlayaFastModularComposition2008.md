---
{"publish":true,"title":"Fast Modular Composition in any Characteristic","created":"2025-05-24T17:36:25.820+01:00","modified":"2025-07-07T22:16:17.516+01:00","published":"2025-07-07T22:16:17.516+01:00","cssclasses":""}
---


# Fast Modular Composition in any Characteristic

>[!meta]- Abstract
- We give an algorithm for modular composition of degree $n$ univariate polynomials over a finite field $\F_q$ requiring $n^{1 + o(1)} \log^{1 + o(1)} q$ bit operations; 
this had earlier been achieved in characteristic $n^{o(1)}$ by Umans (2008). 
- As an application, we obtain a randomized algorithm for factoring degree $n$ polynomials over $\F_q$ requiring $(n^{1.5 + o(1)} + n^{1 + o(1)} \log q) \log^{1 + o(1)} q$ bit operations, improving upon the methods of von zur Gathen & Shoup (1992) and Kaltofen & Shoup (1998). 
- Our results also imply algorithms for 
	- irreducibility testing and 
	- computing minimal polynomials whose running times are best-possible, up to lower order terms.
- As in Umans (2008), we reduce modular composition to certain instances of _multipoint evaluation of multivariate polynomials_. 
	- We then give an algorithm that solves this problem optimally (up to lower order terms), in arbitrary characteristic. 
	- The main idea is to lift to characteristic 0, apply a small number of rounds of multimodular reduction, and finish with a small number of multidimensional FFTs. 
	- The final evaluations are then reconstructed using the Chinese Remainder Theorem. 
- As a bonus, we obtain a very efficient data structure supporting polynomial evaluation queries, which is of independent interest. 
- Our algorithm uses techniques which are commonly employed in practice, so it may be competitive for real problem sizes. This contrasts with previous asymptotically fast methods relying on fast matrix multiplication.

> [!meta]- Metadata
> zotero_link:: [IEEE Xplore Full Text PDF](zotero://select/library/items/F43U5ZRM)
> Authors:: [[people/Kiran S. Kedlaya\|Kiran S. Kedlaya]], [[people/Christopher Umans\|Christopher Umans]], 
> Related:: [[Crossing the logarithmic barrier for dynamic Boolean data structure lower bounds]], 
> url:: https://ieeexplore.ieee.org/document/4690949
> doi:: 
> bibliography:: Kedlaya, Kiran S., and Christopher Umans. 2008. ‘Fast Modular Composition in Any Characteristic’. In _2008 49th Annual IEEE Symposium on Foundations of Computer Science_, 146–55. [https://doi.org/10.1109/FOCS.2008.13](https://doi.org/10.1109/FOCS.2008.13).


---
## Self Notes


Upper bound

Techniques:: Modular Composition, Multipoint Evaluation of Multivariate Polynomials, Lifting to Characteristic 0, Multimodular Reduction, Multidimensional FFTs, Chinese Remainder Theorem
Model:: Static
problems:: [[Problems/Data_Structures/Polynomial Evaluation\|Polynomial Evaluation]]
ubs:: 
  - Optimal running times (up to lower-order terms) for modular composition, polynomial factorization, irreducibility testing, and minimal polynomial computation.

>[!thm] Theorem 4.1. 
>Let $R = (Z/rZ)[Z]/(E(Z))$ be a ring of cardinality $q$, and let $f (X) \in R[X]$ be a degree $n$ polynomial. Choose any constant $\delta > 0$. 
>For sufficiently large $n$, one can compute from the coefficients of $f$ in time at most $T = n^{1+\delta} \log^{1+o(1)} q$ a data structure of size at most $T$ with the following property: 
>- there is an algorithm that given $\alpha \in \F_q$, computes $f(\alpha)$, in time ${\rm poly}\log n ·\log^{1+o(1)} q$ with random access to the data structure.

- Since the algorithm for computing $f$ runs in time at most $T = n^{1+\delta} \log^{1+o(1)} q$, the encoding length is at most $T$. 
- So, this gives a $(S,w,t)$ data structure for Static Polynomial evaluation where $S = n^{1 + \delta} \log^{1+o(1)} q$ , $t = \log^{O(1)} n \cdot \log^{1+o(1)} q$ and $w = \log q$. 

- Multivariate Multipoint Evaluation Algorithm.




## Reading notes



  



