---
{"publish":true,"title":"Cell probe lower bounds and approximations for range mode","created":"2025-05-24T17:36:27.129+01:00","modified":"2025-07-07T14:33:55.244+01:00","published":"2025-07-07T14:33:55.244+01:00","cssclasses":""}
---


# Cell probe lower bounds and approximations for range mode


>[!meta]- Abstract
The mode of a multiset of labels, is a label that occurs at least as often as any other label. 
>- The input to the range mode problem is an array $A$ of size $n$. A range query $[i, j]$ must return the mode of the subarray $A[i], A[i + 1], . . . , A[j]$. 
We prove that any data structure that uses $S$ memory cells of $w$ bits needs $Ω( \log n  \log(Sw/n) )$ time to answer a range mode query. 
>- Secondly, we consider the related range $k$-frequency problem. The input to this problem is an array $A$ of size $n$, and a query $[i, j]$ must return whether there exists a label that occurs precisely $k$ times in the subarray $A[i], A[i+1], . . . , A[j]$. 
We show that for any constant k > 1, this problem is equivalent to 2D orthogonal rectangle stabbing, and that for k = 1 this is no harder than four-sided 3D orthogonal range emptiness. Finally, we consider approximate range mode queries. 
>- A c-approximate range mode query must return a label that occurs at least $1/c$ times that of the mode. We describe a linear space data structure that supports 3-approximate range mode queries in constant time, and a data structure that uses $O( n^ε )$ space and supports $(1 + ε)$-approximation queries  in $O(\log 1/ε )$ time.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/M. Greve\|M. Greve]], [[people/A. Jørgensen\|A. Jørgensen]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Jakob Truelsen\|Jakob Truelsen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Greve, M., A. Jørgensen, Kasper Green Larsen, and Jakob Truelsen. 2010. ‘Cell Probe Lower Bounds and Approximations for Range Mode’. [https://doi.org/10.1007/978-3-642-14165-2_51](https://doi.org/10.1007/978-3-642-14165-2_51).

---
## My Notes


lbs:: $\Omega(\frac{\log n}{\log(sw/n)})$
problems:: [[../../1_Problems/Data_Structures/Static/Range Mode\|Range Mode]] , [[../../1_Problems/Data_Structures/Static/Range k frequency\|Range k frequency]] problem
techniques:: reductions from [[../../1_Problems/Communication_Complexity/SetDisjointness#^f74f8c\|Lopsided Set Disjointness]] and [[../../1_Problems/Data_Structures/Stabbing Queries/2D Rectangle Stabbing\|2D Rectangle Stabbing]]
Model:: Static
InorOut:: In

- For any constant $K > 1$, this is equivalent to [[../../1_Problems/Data_Structures/Stabbing Queries/2D Rectangle Stabbing\|2D Rectangle Stabbing]] , 4-sided 3D othogonal range emptiness. 




