---
{"publish":true,"title":"Semi-direct sum theorem and nearest neighbor under l_infty","created":"2025-05-24T17:36:27.746+01:00","modified":"2025-07-07T15:01:53.144+01:00","published":"2025-07-07T15:01:53.144+01:00","cssclasses":""}
---


# Semi-direct sum theorem and nearest neighbor under l_infty

>[!meta]- Abstract
We introduce semi-direct sum theorem as a framework for proving asymmetric communication lower bounds for the functions of the form $\vee^n_{i=1} f(x, yi)$. Utilizing tools developed in proving direct sum theorem for information complexity, we show that if the function is of the form $\vee^n_{i=1} f(x, yi) where Alice is given $x$ and Bob is given $y_i$’s, it suffices to prove a lower bound for a single $f(x, y_i)$. 
This opens a new avenue of attack other than the conventional combinatorial technique (i.e. “richness lemma” from [12]) for proving randomized lower bounds for asymmetric communication for functions of such form. 
As the main technical result and an application of semi-direct sum framework, we prove an information lower bound on c-approximate Nearest Neighbor (ANN) under `∞ which implies that the algorithm of [9] for c-approximate Nearest Neighbor under `∞ is optimal even under randomization for both decision tree and cell probe data structure model (under certain parameter assumption for the latter). 
In particular, this shows that randomization cannot improve [9] under decision tree model. Previously only a deterministic lower bound was known by [1] and randomized lower bound for cell probe model by [10]. We suspect further applications of our framework in exhibiting randomized asymmetric communication lower bounds for big data applications. 2012 ACM Subject Classification Theory of computation → Communication complexity

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/M. Braverman\|M. Braverman]], [[people/Young Kun-Ko\|Young Kun-Ko]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Braverman, M., and Young Kun-Ko. 2018. ‘Semi-Direct Sum Theorem and Nearest Neighbor under L_infty’. [https://doi.org/10.4230/LIPIcs.APPROX-RANDOM.2018.6](https://doi.org/10.4230/LIPIcs.APPROX-RANDOM.2018.6).

---
## My Notes


Model:: Static    
problems:: Approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#ANN under $ ell_ infty$\|Nearest Neighbour]] Search under $L_\infty$
techniques:: Direct sum theorems for functions of the form $\vee^n_{i=1}f(x,y_i)$.  
lbs::




