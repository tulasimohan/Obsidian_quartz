---
{"publish":true,"title":"A fully dynamic algorithm for recognizing and representing proper interval graphs","created":"2025-05-24T17:36:27.043+01:00","modified":"2025-07-07T14:31:55.455+01:00","published":"2025-07-07T14:31:55.455+01:00","cssclasses":""}
---


# A fully dynamic algorithm for recognizing and representing proper interval graphs


>[!meta]- Abstract
In this paper we study the problem of recognizing and representing dynamically changing proper interval graphs. 
The input to the problem consists of a series of modifications to be performed on a graph, where a modification can be a deletion or an addition of a vertex or an edge. 
The objective is to maintain a representation of the graph as long as it remains a proper interval graph, and to detect when it ceases to be so. 
The representation should enable one to efficiently construct a realization of the graph by an inclusion-free family of intervals. 
This problem has important applications in physical mapping of DNA.
We give a near-optimal fully dynamic algorithm for this problem. It operates in time O(log n) per edge insertion or deletion. 
We prove a close lower bound of ?(log n/(log log n + log b)) amortized time per operation in the cell probe model with word-size b. 
We also construct optimal incremental and decremental algorithms for the problem, which handle each edge operation in O(1) time.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/P. Hell\|P. Hell]], [[people/R. Shamir\|R. Shamir]], [[people/R. Sharan\|R. Sharan]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Hell, P., R. Shamir, and R. Sharan. 1999. ‘A Fully Dynamic Algorithm for Recognizing and Representing Proper Interval Graphs’. [https://doi.org/10.1137/S0097539700372216](https://doi.org/10.1137/S0097539700372216).

---
## My Notes


Model:: Dynamic
problems:: [[Problems/Data_Structures/Dynamic/Recognition and Representation of Interval graphs#^308e20\|proper interval graph recognition]] , [[Problems/Data_Structures/Dynamic/Recognition and Representation of Interval graphs#^4c0951\|connectivity maintenance of interval graphs]]
techniques:: reduction from [[Prefix sum]]
lbs:: $\Omega(\frac{\log n}{\log \log n + b})$ amortized




