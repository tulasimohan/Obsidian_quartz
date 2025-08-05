---
{"publish":true,"title":"Don't rush into a union take time to find your roots","created":"2025-05-24T17:36:27.888+01:00","modified":"2025-07-08T00:07:56.559+01:00","published":"2025-07-08T00:07:56.559+01:00","cssclasses":""}
---


# Don't rush into a union take time to find your roots


>[!meta]- Abstract
We present a new threshold phenomenon in data structure lower bounds where slightly reduced update times lead to exploding query times. 
Consider incremental connectivity, letting $t_u$ be the time to insert an edge and $t_q$ be the query time. 
For $t_u = \Omega(t_q)$, the problem is equivalent to the well-understood union-find problem: proc{InsertEdge}(s,t) can be implemented by Union(Find(s), Find(t)). 
This gives worst-case time $t_u = t_q = O(\lg n / \lg \lg n)$ and amortized $t_u = t_q = O(α(n))$. By contrast, we show that if $t_u = o(\lg n / \lg \lg n)$, the query time explodes to $t_q ≥ n^{1-o(1)}$. In other words, if the data structure doesn't have time to find the roots of each disjoint set (tree) during edge insertion, there is no effective way to organize the information!For amortized complexity, we demonstrate a new inverse-Ackermann type trade-off in the regime $t_u = o(t_q)$.
A similar lower bound is given for fully dynamic connectivity, where an update time of o(lg n) forces the query time to be $n^{1-o(1)}$. This lower bound allows for amortization and Las Vegas randomization, and comes close to the known $O(\lg n • (\lg \lg n)^{O(1)})$ upper bound.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/H64S2FBM)
> Authors:: [[people/Mihai Pătraşcu\|Mihai Pătraşcu]], [[people/Mikkel Thorup\|Mikkel Thorup]], 
> Related:: [[Towards polynomial lower bounds for dynamic problems]], 
> url:: https://dl.acm.org/doi/10.1145/1993636.1993711
> doi:: 
> bibliography:: Pătraşcu, Mihai, and Mikkel Thorup. 2011. ‘Don’t Rush into a Union: Take Time to Find Your Roots’. In _Proceedings of the Forty-Third Annual ACM Symposium on Theory of Computing_, 559–68. STOC ’11. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/1993636.1993711](https://doi.org/10.1145/1993636.1993711).


---
## Self Notes


Model:: Dynamic
problems:: [[Problems/Data_Structures/Dynamic/Connectivity\|Connectivity]] and its [[Resources/Notes/Patrascu, Thorup lowerbound#^d7f2d7\|variant]], [[Problems/Data_Structures/Dynamic/Union-Find\|Union-Find]] problem
Techniques:: [[Techniques/Dynamic/Information Transfer\|Information Transfer]]
lbs:: $t_u = o(\log n) \implies t_q \geq n^{1−o(1)}$



## Reading notes



  
_Imported: 2025-01-19 01:33_

### Theorems and Corollaries

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> THEOREM 2. Any data structure supporting UNION in tU =  o( lg n  lg lg n ) worst-case time and LINK in tL = o( lg n  log tU ) worst-case  time, must have worst-case CONNECTED (and FIND) query time tQ ≥ n1−o(1) in the cell-probe model with cells of O(lg n) bits. >

### Upper and Lowerbounds

Highlight ([page.559](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> For tU = Ω(tq), the problem is equivalent to the well-understood union–find problem >

Highlight ([page.559](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> the classic union-by-rank gives union in constant time and find in O(log n) time >

Highlight ([page.559](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Trade-offs were addressed by Blum [6], with an improvement by Smid [14]. They show that, if the time for union is bounded by tU, FIND can be supported in worst-case O(lg n/ lg tU). >

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> THEOREM 3. Any data structure for fully dynamic connectivity in a graph of n vertices with update time tu = o(lg n) must have query time tq ≥ n1−o(1). >

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Thorup [18] has an almost matching upper bound of tU = O(lg n ·  (lg lg n)3) and tq = o(lg n) >

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> For partial sums and for worst-case union–find, Fredman and Saks showed a lower bound of tq = Ω(lg n/ lg(tU lg n)). For amortized union–find, they gave an optimal inverse-Ackermann lower bound >

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> In STOC’99, Alstrup, Ben-Amram and Rauhe [1] improved the trade-off for union–find to tq = Ω(lg n/ lg tU) >

Note ([page.560](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> In STOC’02, Kaplan, Shafrir and Tarjan [9] showed that the optimal worst-case and amortized trade-offs for union–find also hold for a weaker Boolean version where the user specifies set identifiers and where we only have membership queries. >

Note ([page.561](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> previous strongest bounds from [13] could at most imply tq = Ω(nε) even for constant update time >

Image ([page.565](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> “” could not be found.  
>  



