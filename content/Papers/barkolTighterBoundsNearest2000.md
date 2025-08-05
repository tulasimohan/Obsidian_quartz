---
{"publish":true,"title":"Tighter bounds for nearest neighbor search and related problems in the cell probe model","created":"2025-05-24T17:36:28.921+01:00","modified":"2025-07-11T13:19:42.070+01:00","published":"2025-07-11T13:19:42.070+01:00","cssclasses":""}
---


# Tighter bounds for nearest neighbor search and related problems in the cell probe model


>[!meta]- Abstract
We prove new lower bounds for nearest neighbor search in the Hamming cube. 
Our lower bounds are for randomized, two-sided error, algorithms in Yao's cell probe model. 
Our bounds are in the form of a tradeoff among the number of cells, the size of a cell, and the search time. 
For example, suppose we are searching among n points in the d dimensional cube, we use poly(n, d) cells, each containing poly(d, log n) bits. 
We get a lower bound of Ω(d/log n) on the search time, a significant improvement over the recent bound of Ω(log d) of Borodin et al. 
This should be contrasted with the upper bound of O(log log d) for approximate search (and O(1) for a decision version of the problem; our lower bounds hold in that case). 
By previous results, the bounds for the cube imply similar bounds for nearest neighbor search in high dimensional Euclidean space, and for other geometric problems.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Omer Barkol\|Omer Barkol]], [[people/Y. Rabani\|Y. Rabani]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Barkol, Omer, and Y. Rabani. 2000. ‘Tighter Bounds for Nearest Neighbor Search and Related Problems in the Cell Probe Model’. [https://doi.org/10.1145/335305.335350](https://doi.org/10.1145/335305.335350).

---
## My Notes

Model::Static  
Problems::[[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] search in Hamming cube  
Techniques::  Asymmteric communication, [[Techniques/Static/Richness\|Richness]]
lbs::$Ω(d/log n)$ search time lower bound for poly(n,d) space
InorOut:: In

Randomized lower bounds, technique unknown




