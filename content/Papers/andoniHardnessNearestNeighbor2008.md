---
{"publish":true,"title":"Hardness of Nearest Neighbor under L-infinity","created":"2025-05-24T17:36:29.086+01:00","modified":"2025-07-11T13:24:48.738+01:00","published":"2025-07-11T13:24:48.738+01:00","cssclasses":""}
---


# Hardness of Nearest Neighbor under L-infinity


>[!meta]- Abstract
Recent years have seen a significant increase in our understanding of high-dimensional nearest neighbor search (NNS) for distances like the $l_1$ and $l_2$ norms. 
By contrast, our understanding of the $l_\infty$ norm is now where it was (exactly) 10 years ago. 
In FOCSpsila98, Indyk proved the following unorthodox result: there is a data structure (in fact, a decision tree) of size $O(n\rho)$, for any rho > 1, which achieves approximation $O(\log \rho \log d)$ for NNS in the d-dimensional $l_1$ metric. 
In this paper, we provide results that indicate that Indykpsilas unconventional bound might in fact be optimal. 
Specifically, we show a lower bound for the asymmetric communication complexity of NNS under lscrinfin, which proves that this space/approximation trade-off is optimal for decision trees and for data structures with constant cell-probe complexity.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/VPL64K42)
> Authors:: [[people/Alexandr Andoni\|Alexandr Andoni]], [[people/Dorian Croitoru\|Dorian Croitoru]], [[people/Mihai Patrascu\|Mihai Patrascu]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/abstract/document/4690976
> doi:: 
> bibliography:: Andoni, Alexandr, Dorian Croitoru, and Mihai Patrascu. 2008. ‘Hardness of Nearest Neighbor under L-Infinity’. In _2008 49th Annual IEEE Symposium on Foundations of Computer Science_, 424–33. [https://doi.org/10.1109/FOCS.2008.89](https://doi.org/10.1109/FOCS.2008.89).

---
## My Notes


Model::Static  
Problems:: [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#^418181\|ANN under $\ell_\infty$]]  
Techniques:: [[Techniques/Static/Richness\|Richness]]
lbs::lb matching FOCSpsila98, Indyk upper bound. $\Omega(\log \rho \log d)$. 
model:: cell probe
InorOut:: In

They prove a lower-bound for the cNNS problem, which is ...

- Their argument shows that there exists a product distribution on the rows and columns of the communication matrix, and under this product distribution, any rectangle $A\times B$, where $A$ contains a fraction of $\ge n^{-\alpha}$ rows and $B$ contains a fraction of $\ge 2^{-n^{\delta}}$ columns, will have a $1$ on nearly every column. 
- It follows that any such large rectangle is not $(1 - n^{-\alpha})$-0-monochromatic. (footnote: our $\alpha$ equals the product of the two constants $\rho \delta$ appearing in Theorem 2 of the paper. This is a constant when $c = \Omega(\log \log d)$.) 
- The natural property is then that Barman's algorithm fails to output a ($1 - n^{-\alpha}$)-0-monochromatic rectangle. If there exists an efficient data structure for $f$, then there will exist a large perfectly-0-monochromatic rectangle, and in this case Barman's algorithm succeeds in finding and outputting a ($1-n^{-\alpha}$)-nearly-0-monochromatic rectangle, while running in time $2^{n^{2\alpha} (\log |f|)^2}$, i.e., quasipolynomial in $|f|$. But if $f$ is random, then no such large nearly-monochromatic rectangle exists.

- [ ] TODO: explain why Barman's algorithm works for product distributions





