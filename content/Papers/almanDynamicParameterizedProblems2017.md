---
{"publish":true,"title":"Dynamic parameterized problems and algorithms","created":"2025-05-24T17:36:29.761+01:00","modified":"2025-07-07T14:31:55.452+01:00","published":"2025-07-07T14:31:55.452+01:00","cssclasses":""}
---


# Dynamic parameterized problems and algorithms


>[!meta]- Abstract
Fixed-parameter algorithms and kernelization are two powerful methods to solve NP-hard problems. 
Yet so far those algorithms have been largely restricted to static inputs. 
In this article, we provide fixed-parameter algorithms and kernelizations for fundamental NP-hard problems with dynamic inputs. 
We consider a variety of parameterized graph and hitting set problems that are known to have f(k)n1+o(1) time algorithms on inputs of size n, and we consider the question of whether there is a data structure that supports small updates (such as edge/vertex/set/element insertions and deletions) with an update time of g(k)no(1); such an update time would be essentially optimal. 
Update and query times independent of n are particularly desirable. Among many other results, we show that FEEDBACK VERTEX SET and k-PATH admit dynamic algorithms with f(k)log O(1) update and query times for some function f depending on the solution size k only. 
We complement our positive results by several conditional and unconditional lower bounds. For example, we show that unlike their undirected counterparts, DIRECTED FEEDBACK VERTEX SET and DIRECTED k-PATH do not admit dynamic algorithms with no(1) update and query times even for constant solution sizes k ≤ 3, assuming popular hardness hypotheses. 
We also show that unconditionally, in the cell probe model, DIRECTED FEEDBACK VERTEX SET cannot be solved with update time that is purely a function of k.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Josh Alman\|Josh Alman]], [[people/Matthias Mnich\|Matthias Mnich]], [[people/V. V. Williams\|V. V. Williams]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Alman, Josh, Matthias Mnich, and V. V. Williams. 2017. ‘Dynamic Parameterized Problems and Algorithms’. [https://doi.org/10.1145/3395037](https://doi.org/10.1145/3395037).

---
## My Notes

Model::Dynamic  
Problems:: [[Feedback Vertex Set]], [[k-PATH]]  
Techniques::Parameterized cell probe lower bounds, reductions  
lbs::No o(1)-time algorithms for directed variants (conditional)
InorOut: Out
Reduction, Parametrized. 



