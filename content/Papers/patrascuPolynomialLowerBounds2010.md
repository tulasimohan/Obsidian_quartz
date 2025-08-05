---
{"publish":true,"title":"Towards polynomial lower bounds for dynamic problems","created":"2025-05-24T17:36:27.703+01:00","modified":"2025-07-07T14:33:55.251+01:00","published":"2025-07-07T14:33:55.251+01:00","cssclasses":""}
---


# Towards polynomial lower bounds for dynamic problems


>[!meta]- Abstract
We consider a number of dynamic problems with no known poly-logarithmic upper bounds, and show that they require nΩ(1) time per operation, unless 3SUM has strongly subquadratic algorithms. Our result is modular: (1) We describe a carefully-chosen dynamic version of set disjointness (the "multiphase problem"), and conjecture that it requires n^Omega(1) time per operation. All our lower bounds follow by easy reduction. (2) We reduce 3SUM to the multiphase problem. Ours is the first nonalgebraic reduction from 3SUM, and allows 3SUM-hardness results for combinatorial problems. For instance, it implies hardness of reporting all triangles in a graph. (3) It is plausible that an unconditional lower bound for the multiphase problem can be established via a number-on-forehead communication game.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/PJY3IUHJ)
> Authors:: [[people/Mihai Patrascu\|Mihai Patrascu]], 
> Related:: [[Lower Bounds on Near Neighbor Search via Metric Expansion]], [[Tight bounds for the partial-sums problem]], [[Subcubic equivalences between graph centrality problems, apsp, and diameter]], [[Higher Lower Bounds for Near-Neighbor and Further Rich Problems]], [[Should tables be sorted?]], [[Lower bounds for 2-dimensional range counting]], [[On universal classes of extremely random constant-time hash functions]], [[Don't rush into a union: take time to find your roots]], [[Maximum flow and minimumcost flow in almost-linear time]], [[Negative-weight single-source shortest paths in nearlinear time]], [[Which problems have strongly exponential complexity?]], 
> url:: https://dl.acm.org/doi/10.1145/1806689.1806772
> doi:: 
> bibliography:: Patrascu, Mihai. 2010. ‘Towards Polynomial Lower Bounds for Dynamic Problems’. In _Proceedings of the Forty-Second ACM Symposium on Theory of Computing_, 603–10. STOC ’10. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/1806689.1806772](https://doi.org/10.1145/1806689.1806772).


---
## Self Notes


Model:: Dynamic
Techniques:: reductions from [[3SUM]], [[Multiphase]] conditional lbs 
problems:: dynamic [[Problems/Data_Structures/Dynamic/Reachability\|Reachability]] , dynamic [[Problems/Data_Structures/Dynamic/shortest paths\|Shortest paths]] , [[Problems/Data_Structures/Dynamic/Subgraph connectivity\|Subgraph Connectivity]]  , [[Problems/Data_Structures/Dynamic/Langerman's problem\|Langerman's problem]] , [[Problems/Data_Structures/Dynamic/Pagh's problem\|Pagh's problem]] , [[Problems/Data_Structures/Dynamic/Erikson's problem\|Erikson's problem]]
lbs:: conditional $n^{\Omega(1)}$ lbs



## Reading notes



  
_Imported: 2025-01-19 01:51_

### ❓Open Problems

Note ([page.603](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> It is plausible that an unconditional lower bound for the multiphase problem can be established via a number-onforehead communication game. >  



