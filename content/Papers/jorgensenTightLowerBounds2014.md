---
{"publish":true,"title":"Towards tight lower bounds for range reporting on the RAM","created":"2025-05-24T17:36:27.965+01:00","modified":"2025-07-07T14:31:55.459+01:00","published":"2025-07-07T14:31:55.459+01:00","cssclasses":""}
---


# Towards tight lower bounds for range reporting on the RAM


>[!meta]- Abstract
In the orthogonal range reporting problem, we are to preprocess a set of n points with integer coordinates on a U×U grid. The goal is to support reporting all k points inside an axis-aligned query rectangle. 
This is one of the most fundamental data structure problems in databases and computational geometry. Despite the importance of the problem its complexity remains unresolved in the word-RAM. On the upper bound side, three best tradeoffs exists: (1.) Query time O(n+k) with O(nlg<sup>{</sup>ε}n) words of space for any constant ε>0. (2.) Query time O((1+k)n) with O(nn) words of space. (3.) Query time O((1+k)<sup>{</sup>ε}n) with optimal O(n) words of space. However, the only known query time lower bound is Ω(n+k), even for linear space data structures. All three current best upper bound tradeoffs are derived by reducing range reporting to a ball-inheritance problem. Ball-inheritance is a problem that essentially encapsulates all previous attempts at solving range reporting in the word-RAM. In this paper we make progress towards closing the gap between the upper and lower bounds for range reporting by proving cell probe lower bounds for ball-inheritance. Our lower bounds are tight for a large range of parameters, excluding any further progress for range reporting using the ball-inheritance reduction.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/A. Jørgensen\|A. Jørgensen]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Jørgensen, A., and Kasper Green Larsen. 2014. ‘Towards Tight Lower Bounds for Range Reporting on the RAM’. [https://doi.org/10.4230/LIPIcs.ICALP.2016.92](https://doi.org/10.4230/LIPIcs.ICALP.2016.92).

---
## My Notes


Model:: word RAM model




