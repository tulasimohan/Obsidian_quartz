---
{"publish":true,"created":"2025-05-24T17:36:32.591+01:00","modified":"2025-05-24T17:36:24.412+01:00","published":"2025-05-24T17:36:24.412+01:00","cssclasses":""}
---

# Reachability

>[!DSP] Reachability
>Maintain a directed graph $G$ under:  
>- **updates:** insertions and deletions of edges;
>- **queries:** reachability queries (is there a directed path from u to v?).


[7] C. Demetrescu and G. F. Italiano. Trade-offs for fully dynamic transitive closure on DAGs: breaking through the O(n2) barrier. Journal of the ACM, 52(2):147–156, 2005. See also FOCS’00.

[11] V. King. Fully dynamic algorithms for maintaining all-pairs shortest paths and transitive closure in digraphs. In Proc. 40th IEEE Symposium on Foundations of Computer Science (FOCS), pages 81–91, 1999.

[12] V. King and G. Sagert. A fully dynamic algorithm for maintaining the transitive closure. Journal of Computer and System Sciences, 65(1):150–167, 2002. See also STOC’99.

[17] L. Roditty and U. Zwick. A fully dynamic reachability algorithm for directed graphs with an almost linear update time. In Proc. 36th ACM Symposium on Theory of Computing (STOC), pages 184–191, 2004.

[18] P. Sankowski. Dynamic transitive closure via dynamic matrix inverse. In Proc. 45th IEEE Symposium on Foundations of Computer Science (FOCS), pages 509–517, 2004.



## Reachability in Butterfly Graphs

- First lower bound for reachability.
 
>[!Tip] Theorem 1.2. 
>A reachability oracle using space $S$ in the cell-probe model with $w$-bit cells requires query time $\Omega(\log n/ \log (Sw /n) )$.

- bound is true even for Butterfly Graphs. 
- bound is tight in this special case