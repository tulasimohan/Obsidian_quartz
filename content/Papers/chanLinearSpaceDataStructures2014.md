---
{"publish":true,"title":"Linear-Space Data Structures for Range Mode Query in Arrays","created":"2025-05-24T17:36:29.826+01:00","modified":"2025-07-07T14:31:55.454+01:00","published":"2025-07-07T14:31:55.454+01:00","cssclasses":""}
---


# Linear-Space Data Structures for Range Mode Query in Arrays


>[!meta]- Abstract
A mode of a multiset $S$ is an element $a \in S$ of maximum multiplicity; that is, a occurs at least as frequently as any other element in $S$. 
Given an array A[1:n] of n elements, we consider a basic problem: constructing a static data structure that efficiently answers range mode queries on A. Each query consists of an input pair of indices $(i,j)$ for which a mode of $A[i:j]$ must be returned. 
The best previous data structure with linear space, by Krizanc, Morin, and Smid (Proceedings of the International Symposium on Algorithms and Computation (ISAAC), pp. 517–526, 2003), requires $\Theta (\sqrt{n}\log\log n)$query time in the worst case. 
We improve their result and present an $O(n)$-space data structure that supports range mode queries in $O(\sqrt{n/\log n})$ worst-case time. 
In the external memory model, we give a linear-space data structure that requires $O(\sqrt{n/B})$ I/Os per query, where $B$ denotes the block size. 
Furthermore, we present strong evidence that a query time significantly below $\sqrt{n}$cannot be achieved by purely combinatorial techniques; we show that boolean matrix multiplication of two $\sqrt{n} \times \sqrt{n}$ matrices reduces to $n$ range mode queries in an array of size $O(n)$.

> [!meta]- Metadata
> zotero_link:: [Full Text](zotero://select/groups/5902932/items/67E3U3HD)
> Authors:: [[people/Timothy M. Chan\|Timothy M. Chan]], [[people/Stephane Durocher\|Stephane Durocher]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Jason Morrison\|Jason Morrison]], [[people/Bryan T. Wilkinson\|Bryan T. Wilkinson]], 
> Related:: 
> url:: https://doi.org/10.1007/s00224-013-9455-2
> doi:: 
> bibliography:: Chan, Timothy M., Stephane Durocher, Kasper Green Larsen, Jason Morrison, and Bryan T. Wilkinson. 2014. ‘Linear-Space Data Structures for Range Mode Query in Arrays’. _Theory of Computing Systems_ 55 (4): 719–41. [https://doi.org/10.1007/s00224-013-9455-2](https://doi.org/10.1007/s00224-013-9455-2).

---
## My Notes


InorOut:: Out
Model:: Static, external memory model 
lbs:: upper bound and barrier
Problems:: [[Problems/Data_Structures/Static/Range Mode\|Range Mode]]

Give upper bounds for [[Problems/Data_Structures/Static/Range Mode\|Range Mode]]




