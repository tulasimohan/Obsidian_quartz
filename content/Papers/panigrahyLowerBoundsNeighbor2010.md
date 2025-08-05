---
{"publish":true,"title":"Lower Bounds on Near Neighbor Search via Metric Expansion","created":"2025-05-24T17:36:28.465+01:00","modified":"2025-07-07T22:40:49.140+01:00","published":"2025-07-07T22:40:49.140+01:00","cssclasses":""}
---


# Lower Bounds on Near Neighbor Search via Metric Expansion

>[!meta]- Abstract
>In this paper we show how the complexity of performing nearest neighbor (NNS) search on a metric space is related to the expansion of the metric space. 
>Given a metric space we look at the graph obtained by connecting every pair of points within a certain distance $r$ . 
>We then look at various notions of expansion in this graph relating them to the cell probe complexity of NNS for randomized and deterministic, exact and approximate algorithms. 
>For example if the graph has node expansion $\Phi$ then we show that any deterministic $t$-probe data structure for $n$ points must use space $S$ where $(St/n)^t > \phi$. 
>We show similar results for randomized algorithms as well. These relationships can be used to derive most of the known lower bounds in the well known metric spaces such as l1, l2, l∞, and some new ones, by simply computing their expansion. In the process, we strengthen and generalize our previous results [18].  Additionally, we unify the approach in [18] and the communication complexity based approach. 
>Our work reduces the problem of proving cell probe lower bounds of near neighbor search to computing the appropriate expansion parameter. 
>In our results, as in all previous results, the dependence on t is weak; that is, the bound drops exponentially in t. We show a much stronger (tight) time-space tradeoff for the class of dynamic low contention data structures. 
>These are data structures that supports updates in the data set and that do not look up any single cell too often. A full version of the paper could be found in [19].


> [!meta]- Metadata
> zotero_link:: [IEEE Xplore Full Text PDF](zotero://select/library/items/W8VZ5CRQ)
> Authors:: [[people/Rina Panigrahy\|Rina Panigrahy]], [[people/Kunal Talwar\|Kunal Talwar]], [[people/Udi Wieder\|Udi Wieder]], 
> Related:: [[Adapt or die: Polynomial lower bounds for non-adaptive dynamic data structures]], [[Towards polynomial lower bounds for dynamic problems]], 
> url:: http://ieeexplore.ieee.org/document/5671355/
> doi:: 
> bibliography:: Panigrahy, Rina, Kunal Talwar, and Udi Wieder. 2010. ‘Lower Bounds on Near Neighbor Search via Metric Expansion’. In _2010 IEEE 51st Annual Symposium on Foundations of Computer Science_, 805–14. Las Vegas, NV, USA: IEEE. [https://doi.org/10.1109/FOCS.2010.82](https://doi.org/10.1109/FOCS.2010.82).


---
## Self Notes


Model:: Static
Techniques:: [[Techniques/Static/Cell Sampling\|Cell Sampling]]
problems:: [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] search
lbs:: $t = \tilde\Omega (\log (\frac{S}{n}))$





## Reading notes



  



