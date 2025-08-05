---
{"publish":true,"title":"Randomized Approximate Nearest Neighbor Search with Limited Adaptivity","created":"2025-07-07T16:20:41.764+01:00","modified":"2025-07-07T16:29:09.773+01:00","published":"2025-07-07T16:29:09.773+01:00","cssclasses":""}
---

# Randomized Approximate Nearest Neighbor Search with Limited Adaptivity

>[!meta]- Abstract
We study the problem of approximate nearest neighbor search in $d$-dimensional Hamming space {0,1}d. We study the complexity of the problem in the famous cell-probe model, a classic model for data structures. We consider algorithms in the cell-probe model with limited adaptivity, where the algorithm makes k rounds of parallel accesses to the data structure for a given k. For any k ≥ 1, we give a simple randomized algorithm solving the approximate nearest neighbor search using k rounds of parallel memory accesses, with O(k(log d)1/k) accesses in total. We also give a more sophisticated randomized algorithm using O(k+(1/k log d)O(1/k)) memory accesses in k rounds for large enough k. Both algorithms use data structures of size polynomial in n, the number of points in the database. We prove an Ω(1/k(log d)1/k) lower bound for the total number of memory accesses required by any randomized algorithm solving the approximate nearest neighbor search within k ≤ (log log d)/(2 log log log d) rounds of parallel memory accesses on any data structures of polynomial size. This lower bound shows that our first algorithm is asymptotically optimal for any constant round k. And our second algorithm approaches the asymptotically optimal tradeoff between rounds and memory accesses, in a sense that the lower bound of memory accesses for any k1 rounds can be matched by the algorithm within k2=O(k1) rounds. In the extreme, for some large enough k=Θ((log log d)/(log log log d)), our second algorithm matches the Θ((log log d)/(log log log d)) tight bound for fully adaptive algorithms for approximate nearest neighbor search due to Chakrabarti and Regev.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/4945R2TW)
> Authors:: [[people/Mingmou Liu\|Mingmou Liu]], [[people/Xiaoyin Pan\|Xiaoyin Pan]], [[people/Yitong Yin\|Yitong Yin]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/2935764.2935776
> doi:: 
> bibliography:: Liu, Mingmou, Xiaoyin Pan, and Yitong Yin. 2016. “Randomized Approximate Nearest Neighbor Search with Limited Adaptivity.” In _Proceedings of the 28th ACM Symposium on Parallelism in Algorithms and Architectures_, 23–33. SPAA ’16. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/2935764.2935776](https://doi.org/10.1145/2935764.2935776).

---
## My Notes


model:: Static limited adaptivity
techniques:: [[Techniques/Static/Round elimination\|Round elimination]] of communication protocols for the [[Longest Prefix Matching problem]] (LPM).  
problems:: Approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#Approximate Nearest Neighbour\|Nearest Neighbour]] in the $d$ dimensional Hamming space
lbs:: randomized lb of  $\Omega(\frac1k (\log d)^{1/k} )$ for $k$ rounds of parallel memory access




