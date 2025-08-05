---
{"publish":true,"title":"Using hashing to solve the dictionary problem (in external memory)","created":"2025-05-24T17:36:28.719+01:00","modified":"2025-07-11T13:24:10.409+01:00","published":"2025-07-11T13:24:10.409+01:00","cssclasses":""}
---


# Using hashing to solve the dictionary problem (in external memory)


>[!meta]- Abstract
We consider the dictionary problem in external memory and improve the update time of the well-known [[buffer tree]] by roughly a logarithmic factor. 
For any $λ > \max(\log \log n, \log_{M/B} (n/B)$, we can support updates in time $O(λ/B)$ and queries in sublogarithmic time, $O(\log λ n)$. 
We also present a lower bound in the cell-probe model showing that our data structure is optimal.
In the RAM, hash tables have been use to solve the dictionary problem faster than binary search for more than half a century. 
By contrast, our data structure is the first to beat the comparison barrier in external memory. 
Ours is also the first data structure to depart convincingly from the indivisibility paradigm.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/F2SCAR98)
> Authors:: [[people/John Iacono\|John Iacono]], [[people/Mihai Pătraşcu\|Mihai Pătraşcu]], 
> Related:: 
> url:: https://epubs.siam.org/doi/abs/10.1137/1.9781611973099.48
> doi:: 
> bibliography:: Iacono, John, and Mihai Pătraşcu. 2012. ‘Using Hashing to Solve the Dictionary Problem (in External Memory)’. In _Proceedings of the 2012 Annual Acm-Siam Symposium on Discrete Algorithms (Soda)_, 570–82. Proceedings. Society for Industrial and Applied Mathematics. [https://doi.org/10.1137/1.9781611973099.48](https://doi.org/10.1137/1.9781611973099.48).

---
## My Notes


Model:: Dynamic external memory(large $w$)
Techniques:: [[Techniques/Dynamic/Chronogram\|Chronogram]]
Problems:: [[Problems/Data_Structures/Static/Dictionary\|Dictionary]] 
lbs:: $t_q = \Omega(\log n/\log (Bt_u))$ where the word size $w = O(B \log n)$



The paper gives an upper bound in the RAM model. 
Q: Does external memory correspond to word size $w$ being large? 




