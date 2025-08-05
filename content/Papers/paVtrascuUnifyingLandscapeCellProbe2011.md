---
{"publish":true,"title":"Unifying the Landscape of Cell-Probe Lower Bounds","created":"2025-05-24T17:36:27.267+01:00","modified":"2025-07-13T00:08:06.156+01:00","published":"2025-07-13T00:08:06.156+01:00","cssclasses":""}
---


# Unifying the Landscape of Cell-Probe Lower Bounds

>[!Note] Abstract
- We develop a new technique for proving cell-probe lower bounds on dynamic data structures. 
  This technique enables us to prove an amortized randomized $Ω(\lg⁡ n)$ lower bound per operation for several data structural problems on $n$ elements, including 
	- [[Problems/Data_Structures/Dynamic/Partial Sums\|Partial Sums]], 
	- [[Problems/Data_Structures/Dynamic/Connectivity\|Dynamic Connectivity]] among disjoint paths (or a forest or a graph), 
	- and several other dynamic graph problems (by simple reductions). 
- Such a lower bound breaks a long-standing barrier of $Ω(\lg ⁡n\lg\lg⁡ n)$ for any dynamic language [[Problems/Communication_Complexity/Membership]] problem. 
  It also establishes the optimality of several existing data structures, such as Sleator and Tarjan's dynamic trees. 
- We also prove the first $Ω(\log B⁡n)$ lower bound in the external-memory model without assumptions on the data structure (such as the comparison model). 
- Our lower bounds also give a query-update trade-off curve matched, e.g., by several data structures for dynamic connectivity in graphs. 
- We also prove matching upper and lower bounds for partial sums when parameterized by the word size and the maximum additive change in an update.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Mihai Paˇtraşcu\|Mihai Paˇtraşcu]], 
> Related:: 
> url:: https://epubs.siam.org/doi/10.1137/09075336X
> doi:: 
> bibliography:: Paˇtraşcu, Mihai. 2011. ‘Unifying the Landscape of Cell-Probe Lower Bounds’. _SIAM Journal on Computing_ 40 (3): 827–47. [https://doi.org/10.1137/09075336X](https://doi.org/10.1137/09075336X).


---
### Self Notes

#reduction

Model:: Static and Dynamic
problems::  
techniques:: reduction to Lopsided Set Disjointness 
lbs:: $\Omega(\log n)$

Reduction to Lopsided Set Disjointness 

- Large fraction of DS Lower bounds follow from Lopsided Set Disjointness ([[Problems/Communication_Complexity/SetDisjointness#Lopsided Set Disjointness (LSD)\|LSD]]). 
- Considers three main classes of problems:
	1. high-dimensional problems
	2. constant dimensional geometric problems
	3. dynamic problems (their results for Dynamic problems are slightly weaker)

New results implied from their reductions:
1. $\Omega(\log n/\log \log n)$ bound for [[../../1_Problems/Data_Structures/Both/Range Queries/Range Reporting#4D Range Reporting\|4D Range Reporting]] given space $O(n \cdot \text{polylog}(n))$.
2. A tight space lower bound for [[Problems/Data_Structures/Static/Partial Match]] for constant query time. 
3. The first lower bound for Reachability Oracles
4. Optimal randomized lower bounds for [[Problems/Communication_Complexity/SetDisjointness#Lopsided Set Disjointness (LSD)\|LSD]].

##### High dimensional problems exhibit sharp phase transition.
- either space is linear and the query time is large(linear) or space is quasi-poly and query time is linear
- e.g.: linear search 
- Proved using a technique by Miltersen using Communication Complexity (richness and Round elimination)
If the communication game has a lower bound of $a$, then $S \geq 2^{\Omega(a/t_q)}$. 

##### Constant dimensional geometric problems
- poly-log query time bounds with linear space
- technique by Patrascu and Thorup  Consider a Direct-sum communication game. 


![[Papers/Patrascu Unifying the landscape.png]]


## DS Problems


[[Problems/Data_Structures/Dynamic/Reachability\|Reachability]] in Butterfly graphs
	[[Problems/Data_Structures/Dynamic/Marked Ancestor\|Marked Ancestor]] 
	[[Problems/Data_Structures/Dynamic/2D Skyline Counting\|2D Skyline Counting]]
	[[Problems/Data_Structures/Both/Stabbing_Queries/2D Rectangle Stabbing\|2D Rectangle Stabbing]]
	[[Dynamic 1D stabbing]]
	[[Problems/Data_Structures/Dynamic/Union-Find\|Union-Find]]
	[[Problems/Data_Structures/Dynamic/2D Skyline Counting\|2D Skyline Counting]]
	[[Problems/Data_Structures/Dynamic/Partial Sums\|Partial Sums]]
	Dynamic [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] in 2D
	Dynamic 2D [[Problems/Data_Structures/Both/Range_Queries/Range Counting\|Range Counting]]
	4D [[Problems/Data_Structures/Both/Range_Queries/Range Reporting\|Range Reporting]]	

[[Problems/Data_Structures/Static/Partial Match\|Partial Match]]
$(1+\epsilon)$-Approximate  [[Problems/Data_Structures/Both/Nearest Neighbour]] ANN in $\ell_1,\ell_2$
	[[Problems/Data_Structures/Both/Nearest Neighbour\|Nearest Neighbour]] in $\ell_1,\ell_2$
	3 [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#Approximate Nearest Neighbour\|ANN]] in $\ell_\infty$
	



## CC Problems
Lopsided [[Problems/Communication_Complexity/SetDisjointness\|SetDisjointness]]



## Reading notes



  



