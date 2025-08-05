---
{"publish":true,"title":"Marked ancestor problems","created":"2025-05-24T17:36:29.377+01:00","modified":"2025-07-11T13:18:42.345+01:00","published":"2025-07-11T13:18:42.345+01:00","cssclasses":""}
---


# Marked ancestor problems


>[!meta]- Abstract
Consider a rooted tree whose nodes can be in two states: marked or unmarked. 
The marked ancestor problem is to maintain a data structure with the following operations: mark(v) marks node v: unmark(v) removes any marks from node v; firstmarked(v) returns the first marked node on the path from v to the root. 
We show tight upper and lower bounds for the marked ancestor problem. 
The lower bounds are proved in the cell probe model, the algorithms run on a unit-cost RAM. 
As easy corollaries we prove (often optimal) lower bounds on a number of problems. These include planar range searching, including the existential or emptiness problem, priority search trees static tree union-find, and several problems from dynamic computational geometry, including segment intersection, interval maintenance, and ray shooting in the plane. Our upper bounds improve algorithms from various fields, including coloured ancestor problems and maintenance of balanced parentheses.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Stephen Alstrup\|Stephen Alstrup]], [[people/T. Husfeldt\|T. Husfeldt]], [[people/Theis Rauhe\|Theis Rauhe]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Alstrup, Stephen, T. Husfeldt, and Theis Rauhe. 1998. ‘Marked Ancestor Problems’. [https://doi.org/10.1109/SFCS.1998.743504](https://doi.org/10.1109/SFCS.1998.743504).

---
## My Notes

Model::Dynamic  
Problems:: [[Problems/Data_Structures/Dynamic/Marked Ancestor]] , [[Problems/Data_Structures/Dynamic/Emptiness or Existence\|Emptiness or Existence]] , Static Tree [[Problems/Data_Structures/Dynamic/Union-Find\|Union-Find]] 
Techniques:: modification of [[Techniques/Dynamic/Chronogram\|Chronogram]] 
lbs::Tight $t_q = \Omega(\frac{\log n}{\log (t_u w \log n)})$ 
InorOut: In

- [ ] Read the paper to figure out the lb technique

As corollaries they prove lbs for: 
Planar Range Searching, [[Problems/Data_Structures/Dynamic/Emptiness or Existence\|Emptiness or Existence]] problem, [[Problems/Data_Structures/Solutions/Priority Search Trees\|Priority Search Trees]] , [[Problems/Data_Structures/Dynamic/Union-Find#^32bbc7\|Static Tree Union Find]]

Computational geometry problems: 
[[../../_Problems/Data_Structures/Dynamic/Computational Geometry/Segment intersection\|Segment intersection]] , [[../../_Problems/Data_Structures/Dynamic/Computational Geometry/interval maintanence]] , [[../../_Problems/Data_Structures/Dynamic/Computational Geometry/Ray shooting in the plane]]
 


>[!DDSP] Marked Ancestor Problem
>Consider a rooted tree whose nodes can be in two states: marked or unmarked. 
The marked ancestor problem is to maintain a data structure with the following operations: 
**mark(v)** marks node v: 
**unmark(v)** removes any marks from node v; 
f**irstmarked(v)** returns the first marked node on the path from v to the root.




