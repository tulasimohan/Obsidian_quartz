---
{"publish":true,"title":"Higher Lower Bounds for Near-Neighbor and Further Rich Problems","created":"2025-05-24T17:36:27.556+01:00","modified":"2025-07-11T13:25:07.079+01:00","published":"2025-07-11T13:25:07.079+01:00","cssclasses":""}
---


# Higher Lower Bounds for Near-Neighbor and Further Rich Problems

>[!meta]- Abstract
>- We convert cell-probe lower bounds for polynomial space into stronger lower bound for near-linear space. 
>- Our technique applies to any lower bound proved through the richness method. 
For example, it applies to partial match, and to near-neighbor problems, either for randomized exact search, or for deterministic approximate search (which are thought to exhibit the curse of dimensionality). These problems are motivated by search in large data bases, so near-linear space is the most relevant regime. 
>- Typically, richness has been used to imply $\Omega(d/ \log n)$ lower bounds for polynomial-space data structures, where $d$ is the number of bits of a query. This is the highest lower bound provable through the classic reduction to communication complexity. However, for space $n \log^{O(1)} n$, we now obtain bounds of $\Omega(d/ \log d)$. 
>This is a significant improvement for natural values of $d$, such as $\log^{O(1)} n$. In the most important case of $d = \Theta(\log n)$, we have the first superconstant lower bound. From a complexity-theoretic perspective, our lower bounds are the highest known for any static data-structure problem, significantly improving on previous records.


> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/M3DS3NGI)
> Authors:: [[people/Mihai Patrascu\|Mihai Patrascu]], [[people/Mikkel Thorup\|Mikkel Thorup]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/abstract/document/4031399
> doi:: 
> bibliography:: Patrascu, Mihai, and Mikkel Thorup. 2006. ‘Higher Lower Bounds for Near-Neighbor and Further Rich Problems’. In _2006 47th Annual IEEE Symposium on Foundations of Computer Science (FOCS’06)_, 646–54. [https://doi.org/10.1109/FOCS.2006.35](https://doi.org/10.1109/FOCS.2006.35).


---
## Self Notes


Model:: Static
Problems:: randomised and exact [[../../1_Problems/Data_Structures/Both/Nearest Neighbour\|Nearest Neighbour]], [[../../1_Problems/Data_Structures/Both/Nearest Neighbour#^dfa095\|Approximate Nearest Neighbour]], randomised [[../../1_Problems/Data_Structures/Static/Partial Match\|Partial Match]] , any problem where richness is used
Techniques:: [[Techniques/Static/Richness\|Richness]], Direct sum 
lbs:: improved lbs for near-linear space

| $NN_n^d$              | $\Omega(d/\log \frac{Sd}{n})$                  | randomised and exact       |
| --------------------- | ---------------------------------------------- | -------------------------- |
| $ANN_n^{\gamma,d}$    | $\Omega(\frac{d}{\gamma^3}/\log \frac{Sd}{n})$ | deterministic, approximate |
| Partial match         | $\Omega(\frac{d}{\log d}/\log \frac{Sd}{n})$   | randomised                 |
| inexact Partial match | $\Omega(d/\log(\frac{Sd}n{}))$                 | randomised                 |





| [[Papers/miltersenDataStructuresAsymmetric1998]]                                            | $\Omega(\sqrt{\log d})$ | STOC'95                       | [[../../1_Problems/Data_Structures/Static/Partial Match\|Partial Match]]                  |
| ------------------------------------------------------------------------------------ | ----------------------- | ----------------------------- | -------------------------------------------------------------------------- |
| [[../Unsorted DS_LB/borodinLowerBoundsHigh1999\|borodinLowerBoundsHigh1999]]         | $\Omega(\log d)$        | STOC'99                       | [[../../1_Problems/Data_Structures/Static/Partial Match\|Partial Match]]                  |
| [[../Unsorted DS_LB/barkolTighterBoundsNearest2000\|barkolTighterBoundsNearest2000]] | $\Omega(d/\log n)$      | STOC'00                       | randomized [[../../1_Problems/Data_Structures/Both/Nearest Neighbour\|Nearest Neighbour]] |
| [[Papers/jayramCellprobeLowerBounds2004]]                                                   | $\Omega(d/\log^2n)$     | STOC'03                       | [[../../1_Problems/Data_Structures/Both/Nearest Neighbour\|Nearest Neighbour]]            |
| Ding Liu                                                                             | $\Omega(d)$             | Information Processing Papers | [[../../1_Problems/Data_Structures/Both/Nearest Neighbour\|Nearest Neighbour]]            |
|                                                                                      |                         |                               |                                                                            |

Randomized Approximate NNS

| Chakrabarti, Chazelle, Gum, Lvov                                                                 | STOC'99 |                                       |
| ------------------------------------------------------------------------------------------------ | ------- | ------------------------------------- |
| [[../Unsorted DS_LB/chakrabartiOptimalRandomisedCell2004\|chakrabartiOptimalRandomisedCell2004]] | FOCS'04 | $\Omega(\log \log /\log \log \log d)$ |






## Reading notes



  
_Imported: 2025-04-21 17:42_

### Theorems and Corollaries

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> except that the query must answer “yes” when there exists a neighbor at distance λ, “no” when the nearest neighbor is at least γλ away, and can answer anything otherwise >

### Lemmas

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> partial match >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> near-neighbor problems >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> nearest neighbor search >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The approximate version >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> ANNγ,d >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> partial match problem >

### Upper and Lowerbounds

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> We convert cell-probe lower bounds for polynomial space into stronger lower bound for near-linear space. >

Highlight ([page.1](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> min{ a  lg S , b  w } >  



