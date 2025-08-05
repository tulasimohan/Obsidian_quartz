---
{"publish":true,"title":"Meldable heaps and boolean union-find","created":"2025-05-24T17:36:27.496+01:00","modified":"2025-07-11T13:19:58.935+01:00","published":"2025-07-11T13:19:58.935+01:00","cssclasses":""}
---


# Meldable heaps and boolean union-find


>[!meta]- Abstract
In the classical meldable heap data type we maintain an item-disjoint collection of heaps under the operations find-min, insert, delete, decrease-key, and meld. 
In the usual definition decrease-key and delete get the item and the heap containing it as parameters. 
We consider the modified problem where decrease-key and delete get only the item but not the heap containing it. 
We show that for this problem one of the operations find-min, decrease-key, or meld must take non-constant time. 
This is in contrast with the original data type in which data structures supporting all these three operations in constant time are known (both in an amortized and a worst-case setting).
To establish our results for meldable heaps we consider a weaker version of the union-find problem that is of independent interest, which we call Boolean union-find. 
In the Boolean union-find problem the find operation is a binary predicate that gets an item x and a set A and answers positively if and only if &khgr; ε A.
We prove that the lower bounds which hold for union-find in the cell probe model hold for Boolean union-find as well.
We also suggest new heap data structures implementing the modified meldable heap data type that are based on redundant binary counters. Our data structures have good worst-case bounds. The best of our data structures matches the worst-case lower bounds which we establish for the problem. 
The simplest of our data structures is an interesting generalization of binomial queues.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Haim Kaplan\|Haim Kaplan]], [[people/Nira Shafrir\|Nira Shafrir]], [[people/R. Tarjan\|R. Tarjan]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Kaplan, Haim, Nira Shafrir, and R. Tarjan. 2002. ‘Meldable Heaps and Boolean Union-Find’. [https://doi.org/10.1145/509907.509990](https://doi.org/10.1145/509907.509990).

---
## My Notes


problems:: [[Problems/Data_Structures/Dynamic/Union-Find#^4f4a4d\|Boolean Union-Find]] , [[Problems/Data_Structures/Solutions/Meldable heap\|Meldable heap]] problem
techniques:: [[Techniques/Dynamic/Chronogram\|Chronogram]]
lbs:: $t_q = \Omega(\frac{\log n}{\log t_u})$
Model:: Dynamic
InorOut:: In




