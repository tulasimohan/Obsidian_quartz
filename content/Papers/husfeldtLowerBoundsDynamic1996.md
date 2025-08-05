---
{"publish":true,"title":"Lower bounds for dynamic transitive closure, planar point location, and parentheses matching","created":"2025-05-24T17:36:29.140+01:00","modified":"2025-07-11T13:18:25.429+01:00","published":"2025-07-11T13:18:25.429+01:00","cssclasses":""}
---


# Lower bounds for dynamic transitive closure, planar point location, and parentheses matching


>[!meta]- Abstract
We give a number of new lower bounds in the cell probe model with logarithmic cell size, which entails the same bounds on the random access computer with logarithmic word size and unit cost operations.
We study the signed prefix sum problem~ given a string of length n of 0s and signed ls, compute the sum of its ith prefix during updates. We show a lower bound of ~(log n/log log n) time per operations, even if the  prefix sums are bounded by log n/log log n during all updates. We also show that if the update time is bounded by the product of the worst-case update time and the answer to the query, then the update time must be f~(x/(log n~log log n)). These results allow us to prove lower bounds for a variety of seemingly unrelated dynamic problems. We give a lower bound for the dynamic planar point location in monotone subdivisions of f~(log n~log log n) per operation. We give a lower bound for dynamic transitive closure on upward planar graphs with one source and one sink of ~(log n/(log log n) 2) per operation. We give a lower bound of 12(~/(log n/log log n)) for the dynamic membership problem of any Dyck language with two or more letters. This implies the same lower bound for the dynamic word problem for the free group with k generators. We also give lower bounds for the dynamic prefix majority and prefix equality problems.


> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/YIGHY9Q4)
> Authors:: [[people/Thore Husfeldt\|Thore Husfeldt]], [[people/Theis Rauhe\|Theis Rauhe]], [[people/Søren Skyum\|Søren Skyum]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Husfeldt, Thore, Theis Rauhe, and Søren Skyum. 1996. ‘Lower Bounds for Dynamic Transitive Closure, Planar Point Location, and Parentheses Matching’. In _Algorithm Theory — SWAT’96_, edited by Rolf Karlsson and Andrzej Lingas, 198–211. Berlin, Heidelberg: Springer. [https://doi.org/10.1007/3-540-61422-2_132](https://doi.org/10.1007/3-540-61422-2_132).

---
## My Notes


Model:: Dynamic
techniques::[[Techniques/Dynamic/Chronogram\|Chronogram]] and Reductions
problems:: [[Problems/Data_Structures/Dynamic/Partial Sums\|Prefix sum]], [[Membership of Dyck language]]
lbs::

- [ ] To read 
- Techniques Look like Chronogram and Reductions. 




