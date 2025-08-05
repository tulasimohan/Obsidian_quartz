---
{"publish":true,"title":"Super-Logarithmic Lower Bounds for Dynamic Graph Problems","created":"2025-05-24T17:36:29.781+01:00","modified":"2025-07-07T22:42:53.130+01:00","published":"2025-07-07T22:42:53.130+01:00","cssclasses":""}
---


# Super-Logarithmic Lower Bounds for Dynamic Graph Problems


>[!meta]- Abstract
In this work, we prove a \tildeØmega(łg^3/2 n) unconditional lower bound on the maximum of the query time and update time for dynamic data structures supporting reachability queries in n-node directed acyclic graphs under edge insertions. This is the first super-logarithmic lower bound for any natural graph problem. In proving the lower bound, we also make novel contributions to the state-of-the-art data structure lower bound techniques that we hope may lead to further progress in proving lower bounds.

> [!meta]- Metadata
> zotero_link:: [Submitted Version](zotero://select/library/items/TRK6PHCN)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Huacheng Yu\|Huacheng Yu]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/document/10353102
> doi:: 
> bibliography:: Larsen, Kasper Green, and Huacheng Yu. 2023. ‘Super-Logarithmic Lower Bounds for Dynamic Graph Problems’. In _2023 IEEE 64th Annual Symposium on Foundations of Computer Science (FOCS)_, 1589–1604. [https://doi.org/10.1109/FOCS57990.2023.00096](https://doi.org/10.1109/FOCS57990.2023.00096).


---
## Self Notes



Model:: Dynamic
Techniques:: [[Techniques/Dynamic/chronogram + cell sampling + Peak to average\|chronogram + cell sampling + Peak to average]] , Butterfly graphs
lbs:: $\tilde\Omega(\log^{1.5} n)$
problems:: [[Problems/Data_Structures/Dynamic/Reachability\|Reachability]], [[0-XOR is Butterfly graphs]]



## Reading notes



  
_Imported: 2025-01-19 01:49_

### Theorems and Corollaries

Note ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Theorem 1. Any data structure for Dynamic Reachability in n-node directed acyclic graphs under edge insertions, with worst case update time tu, expected query time tq and w-bit memory cells for w = Ω(lg n), must satisfy  tq = Ω  (  lg3/2 n  lg2(tuw)  )  . >

### Upper and Lowerbounds

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The strongest known unconditional lower bound for any natural graph problem, is an Ω(lg n) >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Ω ̃ (lg2 n) lower bounds for dynamic problems with Ω(lg n)-bit outputs to queries >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Ω ̃ (lg3/2 n) lower bounds for dynamic decision problems (1-bit outputs) due to Larsen, Weinstein and Yu >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Paˇtras ̧cu and Thorup [17] showed that for Dynamic Reachability, even in the undirected case, any data structure with update time tu = o(lg n) must  ∗larsen@cs.au.dk. Supported by a DFF Sapere Aude Research Leader Grant No. 9064-00068B. †yuhch123@gmail.com. Supported by Simons Junior Faculty Award - AWD1007164.  1  arXiv:2304.08745v1 [cs.DS] 18 Apr 2023 have query time tq = n1−o(1) >

Highlight ([page.2](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The current state-of-the-art technique for proving lower bounds for static data structures, is the cell sampling technique by Panigrahy et al. [11] that was later refined in [9] >

Highlight ([page.4](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Building on the chronogram technique, Larsen [8] later developed a technique capable of proving lower bounds of tq = Ω((lg n/ lg(tuw))2) for dynamic data structures. >

Highlight ([page.7](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Pˇatra ̧scu [12] in his seminal work that established lower bounds for a host of static data structure problems >  



