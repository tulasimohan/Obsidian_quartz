
Priority searching, a mixture of a *search structure* and a *priority queue*, 
supports the following operations 

>[!DS] Priority Search Tree 
>**Data:** on a set of points $X \subseteq [n]$ with priorities $p(n) \in [n]$,  
**Updates:** 
>	***insert$(x, p(x))$:*** insert $x$ into $X$ with priority $p(x)$,  
>	***delete(x):*** remove $x$ from $X$  
**Queries:**	
>	***max(x):*** return $\max \{ p(y) | y \leq x \}$.
	