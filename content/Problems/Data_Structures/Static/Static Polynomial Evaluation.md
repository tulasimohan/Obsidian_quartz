## Problem statement

>[!DSP] $P(n,q)$
>**Data**: Polynomials $P$ over $\F_q$ of degree $n$.
>**Queries**: $x \in \F_q$ output $P(x)$. 

> Size of the instance  and parameters, 
> - Typically $q=n^2 =n^{O(1)}$, 
> - N:: $q^n = 2^{O(n\log n)}$,
> - M:: $q = 2^{O(\log n)}$.

## Upper bounds

- Kendalaya, Umans  [[Papers/kedlayaFastModularComposition2008\|kedlayaFastModularComposition2008]] give a $(S,w,t)$ data-structure for 
	- $S = n^{1 + \delta}\log^{1+o(1)} q$ for all $\delta > 0$, 
	- $t = \log^{O(1)} n \cdot \log^{1+o(1)} q$,
	- $w = O(\log n )$.
- 

## Lower bounds
