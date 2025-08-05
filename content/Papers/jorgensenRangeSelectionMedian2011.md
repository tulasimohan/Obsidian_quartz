---
{"publish":true,"title":"Range selection and median tight cell probe lower bounds and adaptive data structures","created":"2025-05-24T17:36:29.470+01:00","modified":"2025-07-08T12:06:42.444+01:00","published":"2025-07-08T12:06:42.444+01:00","cssclasses":""}
---


# Range selection and median tight cell probe lower bounds and adaptive data structures

>[!meta]- Abstract
*Range selection* is the problem of preprocessing an input array $A$ of $n$ unique integers, such that given a query $(i, j, k)$, one can report the $k^{th}$ smallest integer in the subarray $A[i], A[i + 1], …, A[j]$. 
In this paper we consider static data structures in the word-RAM for range selection and several natural special cases thereof.
>- The first special case is known as *range median*, which arises when $k$ is fixed to $⌊(j − i + 1)/2⌋$. 
>- The second case, denoted *prefix selection*, arises when $i$ is fixed to 0. 
>- Finally, we also consider the *bounded rank prefix selection* problem and the *fixed rank range selection* problem. In the former, data structures must support prefix selection queries under the assumption that $k ≤ κ$ for some value $κ ≤ n$ given at construction time, while in the latter, data structures must support range selection queries where $k$ is fixed beforehand for all queries. 
>
>- We prove cell probe lower bounds for range selection, prefix selection and range median, stating that any data structure that uses S words of space needs $Ω(\log n/\log(Sw/n))$ time to answer a query. 
>	-In particular, any data structure that uses $n{\log^{O(1)} n}$  space needs $Ω(\log n/ \log \log n)$ time to answer a query, and any data structure that supports queries in constant time, needs $n^{1+Ω(1)}$ space. 
>-For data structures that uses $n{\log^{O(1)} n}$ space this matches the best known upper bound.
>	-Additionally, we present a linear space data structure that supports range selection queries in $O(\log k/\log \log n + \log \log n)$ time. 
>- Finally, we prove that any data structure that uses $S$ space, needs $Ω(\log κ/\log(Sw/n))$ time to answer a bounded rank prefix selection query and $Ω(\log k/\log(Sw/n))$ time to answer a fixed rank range selection query. This shows that our data structure is optimal except for small values of $k$.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/A. Jørgensen\|A. Jørgensen]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Jørgensen, A., and Kasper Green Larsen. 2011. ‘Range Selection and Median: Tight Cell Probe Lower Bounds and Adaptive Data Structures’. [https://doi.org/10.1137/1.9781611973082.63](https://doi.org/10.1137/1.9781611973082.63).

---
## My Notes


Model:: Static 
techniques:: same as [[Papers/pVatrascuLowerBounds2dimensional2007\|pVatrascuLowerBounds2dimensional2007]], dominance counting 
problems:: [[Problems/Data_Structures/Static/Range selection\|Range selection]], [[Prefix selection]], [[Bounded rank prefix selection]], [[Fixed rank range selection]]
lbs:: $\Omega(\frac{\log n}{\log (Sw/n)})$

- [ ] what is Dominance counting ?
- [ ] to read, uses bit-reversal order.  



