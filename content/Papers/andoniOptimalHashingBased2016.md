---
{"publish":true,"title":"Optimal hashing-based time-space trade-offs for approximate near neighbors","created":"2025-05-24T17:36:28.953+01:00","modified":"2025-07-07T15:01:53.140+01:00","published":"2025-07-07T15:01:53.140+01:00","cssclasses":""}
---


# Optimal hashing-based time-space trade-offs for approximate near neighbors


>[!meta]- Abstract
[See the paper for the full abstract.] We show tight upper and lower bounds for time-space trade-offs for the c-Approximate Near Neighbor Search problem. 
For the d-dimensional Euclidean space and n-point datasets, we develop a data structure with space n<sup>{</sup>1+ρ<sub>u</sub>+o(1)}+O(dn) and query time n<sup>{</sup>ρ<sub>q</sub>+o(1)}+dn<sup>{</sup>o(1)} for every ρ<sub>u</sub>,ρ<sub>q</sub>≥0 such that: {equation} c^2 √{ρ_q} + (c^2 - 1) √{ρ_u} = √{2c^2 - 1}. {equation} 
This is the first data structure that achieves sublinear query time and near-linear space for every approximation factor c>1, improving upon [Kapralov, PODS 2015]. The data structure is a culmination of a long line of work on the problem for all space regimes; it builds on Spherical Locality-Sensitive Filtering [Becker, Ducas, Gama, Laarhoven, SODA 2016] and data-dependent hashing [Andoni, Indyk, Nguyen, Razenshteyn, SODA 2014] [Andoni, Razenshteyn, STOC 2015]. 
Our matching lower bounds are of two types: conditional and unconditional. 
First, we prove tightness of the whole above trade-off in a restricted model of computation, which captures all known hashing-based approaches. 
We then show unconditional cell-probe lower bounds for one and two probes that match the above trade-off for ρ<sub>q</sub>=0, improving upon the best known lower bounds from [Panigrahy, Talwar, Wieder, FOCS 2010]. 
In particular, this is the first space lower bound (for any static data structure) for two probes which is not polynomially smaller than the one-probe bound. 
To show the result for two probes, we establish and exploit a connection to locally-decodable codes.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Alexandr Andoni\|Alexandr Andoni]], [[people/Thijs Laarhoven\|Thijs Laarhoven]], [[people/Ilya P. Razenshteyn\|Ilya P. Razenshteyn]], [[people/Erik Waingarten\|Erik Waingarten]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Andoni, Alexandr, Thijs Laarhoven, Ilya P. Razenshteyn, and Erik Waingarten. 2016. ‘Optimal Hashing-Based Time-Space Trade-Offs for Approximate near Neighbors’. [https://doi.org/10.1137/1.9781611974782.4](https://doi.org/10.1137/1.9781611974782.4).

---
## My Notes

Model::Static  
Problems:: Approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]]  
Techniques::connection to locally-decodable codes
lbs:: first lower bound on space for 2 probes which is not plynomially smaller than 1 probe. Improves on PTW2010 for 2 probes.   
InorOut:: In

Barely in because the bounds hold for only two probes. 
Interesting because of the connection to LDCs.  



