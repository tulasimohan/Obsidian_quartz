---
{"publish":true,"title":"Fully dynamic cycle-equivalence in graphs","created":"2025-05-24T17:36:28.059+01:00","modified":"2025-07-07T14:31:55.449+01:00","published":"2025-07-07T14:31:55.449+01:00","cssclasses":""}
---


# Fully dynamic cycle-equivalence in graphs


>[!meta]- Abstract
Two edges e/sub 1/ and e/sub 2/ of an undirected graph are cycle-equivalent iff all cycles that contain e/sub 1/ also contain e/sub 2/, i.e., iff e/sub 1/ and e/sub 2/ are a cut-edge pair. The cycle-equivalence classes of the control-flow graph are used in optimizing compilers to speed up existing control-flow and data-flow algorithms. While the cycle-equivalence classes can be computed in linear time, we present the first fully dynamic algorithm for maintaining the cycle-equivalence relation. In an n-node graph our data structure executes an edge insertion or deletion in O(/spl radic/n log n) time and answers the query whether two given edges are cycle-equivalent in O(log/sup 2/ n) time. We also present an algorithm for plane graphs with O(log n) update and query time and for planar graphs with O(log n) insertion time and O(log/sup 2/ n) query and deletion time. Additionally, we show a lower bound of /spl Omega/(log n/log log n) for the amortized time per operation for the dynamic cycle-equivalence problem in the cell probe model.«ETX»

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Monika Henzinger\|Monika Henzinger]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Henzinger, Monika. 1994. ‘Fully Dynamic Cycle-Equivalence in Graphs’. [https://doi.org/10.1109/SFCS.1994.365718](https://doi.org/10.1109/SFCS.1994.365718).

---
## My Notes


Model:: Dynamic
problems:: Dynamic [[Cycle equivalence]] problem
techniques:: reduction to [[../../1_Problems/Data_Structures/Static/Prefix Parity\|Prefix Parity]]  
lbs:: $\Omega(\log n/\log \log n + \log b)$
InorOut:: Out




