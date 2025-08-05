---
{"publish":true,"title":"The cell probe complexity of dynamic range counting","created":"2025-05-24T17:36:27.331+01:00","modified":"2025-07-07T22:12:06.550+01:00","published":"2025-07-07T22:12:06.550+01:00","cssclasses":""}
---


# The cell probe complexity of dynamic range counting

>[!meta]- Abstract
In this paper we develop a new technique for proving lower bounds on the update time and query time of dynamic data structures in the cell probe model. With this technique, we prove the highest lower bound to date for any explicit problem, namely a lower bound of tq=Ω((lg n/lg(wtu))2). Here n is the number of update operations, w the cell size, tq the query time and tu the update time. In the most natural setting of cell size w=Θ(lg n), this gives a lower bound of tq=Ω((lg n/lg lg n)2) for any polylogarithmic update time. This bound is almost a quadratic improvement over the highest previous lower bound of Ω(lg n), due to Patrascu and Demaine [SICOMP'06].We prove our lower bound for the fundamental problem of weighted orthogonal range counting. In this problem, we are to support insertions of two-dimensional points, each assigned a Θ(lg n)-bit integer weight. A query to this problem is specified by a point q=(x,y), and the goal is to report the sum of the weights assigned to the points dominated by q, where a point (x',y') is dominated by q if x' ≤ x and y' ≤ y. In addition to being the highest cell probe lower bound to date, our lower bound is also tight for data structures with update time tu = Ω(lg2+εn), where ε&gt;0 is an arbitrarily small constant.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/R4HQJPC4)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/2213977.2213987
> doi:: 
> bibliography:: Larsen, Kasper Green. 2012. ‘The Cell Probe Complexity of Dynamic Range Counting’. In _Proceedings of the Forty-Fourth Annual ACM Symposium on Theory of Computing_, 85–94. STOC ’12. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/2213977.2213987](https://doi.org/10.1145/2213977.2213987).


---
## Self Notes


Techniques:: [[Techniques/Dynamic/Chronogram + Cell sampling\|Chronogram + Cell sampling]]
Model:: Dynamic
problems:: Weighted [[Problems/Data_Structures/Both/Range_Queries/Orthogonal Range Counting\|Range counting]]
lbs:: $t_q = Ω((\frac{\lg n}{ \lg(w t_u)})^2)$.
 


## Reading notes



  



