---
{"publish":true,"title":"Adapt or die Polynomial lower bounds for non-adaptive dynamic data structures","created":"2025-05-24T17:36:28.326+01:00","modified":"2025-07-07T14:31:55.452+01:00","published":"2025-07-07T14:31:55.452+01:00","cssclasses":""}
---


# Adapt or die Polynomial lower bounds for non-adaptive dynamic data structures


>[!meta]- Abstract
In this paper, we study the role non-adaptivity plays in maintaining dynamic data structures. Roughly speaking, a data structure is non-adaptive if the memory locations it reads and/or writes when processing a query or update depend only on the query or update and not on the contents of previously read cells. We study such non-adaptive data structures in the cell probe model. The cell probe model is one of the least restrictive lower bound models and in particular, cell probe lower bounds apply to data structures developed in the popular word-RAM model. Unfortunately, this generality comes at a high cost: the highest lower bound proved for any data structure problem is only polylogarithmic (if allowed adaptivity). Our main result is to demonstrate that one can in fact obtain polynomial cell probe lower bounds for non-adaptive data structures. To shed more light on the seemingly inherent polylogarithmic lower bound barrier, we study several different notions of non-adaptivity and identify key properties that must be dealt with if we are to prove polynomial lower bounds without restrictions on the data structures. Finally, our results also unveil an interesting connection between data structures and depth-2 circuits. This allows us to translate conjectured hard data structure problems into good candidates for high circuit lower bounds; in particular, in the area of linear circuits for linear operators. Building on lower bound proofs for data structures in slightly more restrictive models, we also present a number of properties of linear operators which we believe are worth investigating in the realm of circuit lower bounds.

> [!meta]- Metadata
> zotero_link:: [Theory of computing Full Text PDF](zotero://select/groups/5902932/items/QRK3JPLX)
> Authors:: [[people/Joshua Brody\|Joshua Brody]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: https://theoryofcomputing.org/articles/v011a019/
> doi:: 
> bibliography:: Brody, Joshua, and Kasper Green Larsen. 2015. ‘Adapt or Die: Polynomial Lower Bounds for Non-Adaptive Dynamic Data Structures’. _Theory of Computing_ 11 (December):471–89. [https://doi.org/10.4086/toc.2015.v011a019](https://doi.org/10.4086/toc.2015.v011a019).

---
## My Notes


- Model:: Dynamic    
- problems:: [[Problems/Data_Structures/Dynamic/Indexing\|Indexing]], [[Problems/Communication_Complexity/SetDisjointness\|SetDisjointness]]
- techniques:: Non-adaptive encoding, Memoryless encoding 
- lbs:: polynomial lower bounds for non-adaptive and memory less




