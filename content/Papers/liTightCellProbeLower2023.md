---
{"publish":true,"title":"Tight Cell-Probe Lower Bounds for Dynamic Succinct Dictionaries","created":"2025-05-25T01:18:14.769+01:00","modified":"2025-07-08T00:07:24.260+01:00","published":"2025-07-08T00:07:24.260+01:00","cssclasses":""}
---


# Tight Cell-Probe Lower Bounds for Dynamic Succinct Dictionaries


>[!meta]- Abstract
A dictionary data structure maintains a set of at most n keys from the universe [U] under key insertions and deletions, such that given a query x ın[U], it returns if x is in the set. Some variants also store values associated to the keys such that given a query x, the value associated to x is returned when x is in the set.This fundamental data structure problem has been studied for six decades since the introduction of hash tables in 1953. A hash table occupies O(n łog U) bits of space with constant time per operation in expectation. There has been a vast literature on improving its time and space usage. The state-of-the-art dictionary by Bender, Farach-Colton, Kuszmaul, Kuszmaul and Liu [1] has space consumption close to the information-theoretic optimum, using a total of \beginequation*łog \beginpmatrix U \ n \endpmatrix+Onłog ^łeft(k\right) n\endequation* bits, while supporting all operations in O(k) time, for any parameter k łeq łog ^* n. The term Ołeft(łog ^(k) n\right)=O(\underbracełog \cdots łog n) is referred to as the wasted bits per key.In this paper, we prove a matching cell-probe lower bound: For U=n<sup>1+\Theta(1)</sup>, any dictionary with Ołeft(łog ^(k) n\right) wasted bits per key must have expected operational time Ømega(k), in the cell-probe model with word-size w=\Theta(łog U). Furthermore, if a dictionary stores values of \Theta(łog U) bits, we show that regardless of the query time, it must have Ømega(k) expected update time. It is worth noting that this is the first cell-probe lower bound on the trade-off between space and update time for general data structures.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/FK5ITAYA)
> Authors:: [[people/Tianxiao Li\|Tianxiao Li]], [[people/Jingxun Liang\|Jingxun Liang]], [[people/Huacheng Yu\|Huacheng Yu]], [[people/Renfei Zhou\|Renfei Zhou]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/document/10353191
> doi:: 
> bibliography:: Li, Tianxiao, Jingxun Liang, Huacheng Yu, and Renfei Zhou. 2023. ‘Tight Cell-Probe Lower Bounds for Dynamic Succinct Dictionaries’. In _2023 IEEE 64th Annual Symposium on Foundations of Computer Science (FOCS)_, 1842–62. [https://doi.org/10.1109/FOCS57990.2023.00112](https://doi.org/10.1109/FOCS57990.2023.00112).

---
## My Notes


model:: Dynamic
techniques::[[Techniques/Dynamic/Information Transfer\|Information Transfer]]
problems:: [[Problems/Data_Structures/Static/Dictionary\|Dictionary]]
lbs:: see abstract




