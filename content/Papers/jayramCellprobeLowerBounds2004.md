---
{"publish":true,"title":"Cell-probe lower bounds for the partial match problem","created":"2025-05-24T17:36:27.240+01:00","modified":"2025-07-11T13:21:58.745+01:00","published":"2025-07-11T13:21:58.745+01:00","cssclasses":""}
---


# Cell-probe lower bounds for the partial match problem


>[!meta]- Abstract
>Given a database of $n$ points in $\{0,1\}^d$, the partial match problem is: In response to a query $x \in \{0, 1, *\}^d$, find a database point $y$ such that for every $i$ whenever $x_i \neq *$, we have $x_i = y_i$. 
>In this paper we show randomized lower bounds in the cell-probe model for this well-studied problem[18, 11, 19, 16, 4, 6 ]. Our lower bounds follow from a two-party asymmetric randomized communication complexity near-optimal lower bound for this problem, where we show that either Alice has to send Ω(d log n) bits or Bob has to send Ω(n1 - o(1)) bits. When applied to the cell-probe model, it means that if the number of cells is restricted to be poly(n, d) where each cell is of size poly(log n, d), then Ω(d/log2 n) probes are needed. This is an exponential improvement over the previously known lower bounds for this problem[16, 4].$


> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/T. S. Jayram\|T. S. Jayram]], [[people/Subhash Khot\|Subhash Khot]], [[people/Ravi Kumar\|Ravi Kumar]], [[people/Yuval Rabani\|Yuval Rabani]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Jayram, T. S., Subhash Khot, Ravi Kumar, and Yuval Rabani. 2004. ‘Cell-Probe Lower Bounds for the Partial Match Problem’. _Journal of Computer and System Sciences_ 69 (3): 435–47. [https://doi.org/10.1016/j.jcss.2004.04.006](https://doi.org/10.1016/j.jcss.2004.04.006).


---
## Self Notes


>[!DSP] Partial Match
>**Data:** Given a database of $n$ points in $\{0,1\}^d$, the partial match problem is: 
>**Query:** For $x \in \{0, 1, *\}^d$, find a database point $y$ such that for every $i$ whenever $x_i \neq *$, we have $x_i = y_i$. 

Techniques:: [[Techniques/Static/Richness\|Richness]], Randomized Asymmetric communication
Model:: Static
problems:: [[Problems/Data_Structures/Static/Partial Match\|Partial Match]] Problem, [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] in $\ell_\infty$
lbs:: $\Omega(d / \log^2 n)$ 

- Lower bounds hold even for polynomial space data structures.



## Reading notes



  



