---
{"publish":true,"title":"Non-adaptive data structure bounds for dynamic predecessor","created":"2025-05-24T17:36:27.866+01:00","modified":"2025-07-07T16:38:08.641+01:00","published":"2025-07-07T16:38:08.641+01:00","cssclasses":""}
---


# Non-adaptive data structure bounds for dynamic predecessor


>[!meta]- Abstract
In this work, we continue the examination of the role non-adaptivity plays in maintaining dynamic data structures, initiated by Brody and Larsen. 
We consider non-adaptive data structures for predecessor search in the w-bit cell probe model. 
In this problem, the goal is to dynamically maintain a subset T of up to n elements from {1, ..., m}, while supporting insertions, deletions, and a predecessor query Pred(x), which returns the largest element in T that is less than or equal to x. 
Predecessor search is one of the most well-studied data structure problems. 
For this problem, using non-adaptivity comes at a steep price. 
We provide exponential cell probe complexity separations between 
(i) adaptive and non-adaptive data structures and (ii) non-adaptive and memoryless data structures for predecessor search. 
A classic data structure of van Emde Boas solves dynamic predecessor search in log(log(m)) probes; this data structure is adaptive. 
For dynamic data structures which make non-adaptive updates, we show the cell probe complexity is O(log(m)/log(w/log(m))). We also give a nearly-matching Omega(log(m)/log(w)) lower bound. We also give an m/w lower bound for memoryless data structures. Our lower bound technique is tailored to non-adaptive (as opposed to memoryless) updates and might be of independent interest.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Joseph Boninger\|Joseph Boninger]], [[people/Joshua Brody\|Joshua Brody]], [[people/O. Kephart\|O. Kephart]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Boninger, Joseph, Joshua Brody, and O. Kephart. 2017. ‘Non-Adaptive Data Structure Bounds for Dynamic Predecessor’. [https://doi.org/10.4230/LIPIcs.FSTTCS.2017.20](https://doi.org/10.4230/LIPIcs.FSTTCS.2017.20).

---
## My Notes


Model::Dynamic  Non-adaptive and Memory less updates
Problems::[[Problems/Data_Structures/Both/Predecessor\|Predecessor]] search  
Techniques::Non-adaptive, Memoryless ideas from [[brody_adapt_2015]][[brody_adapt_2015]]
lbs::$Ω(\log m/\log w)$ for non-adaptive and $\Omega(n/w)$ for memory-less updates. 




