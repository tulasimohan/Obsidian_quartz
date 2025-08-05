---
{"publish":true,"title":"Lower Bounds for Oblivious Near-Neighbor Search","created":"2025-07-07T16:42:16.150+01:00","modified":"2025-07-07T16:53:30.657+01:00","published":"2025-07-07T16:53:30.657+01:00","cssclasses":""}
---

# Lower Bounds for Oblivious Near-Neighbor Search

>[!meta]- Abstract
We prove an Ω(d lg n/(lg lg n)2) lower bound on the dynamic cell-probe complexity of statistically oblivious approximate-near-neighbor search (ANN) over the d-dimensional Hamming cube. For the natural setting of d = Θ(lg n), our result implies an  lower bound, which is a quadratic improvement over the highest (non-oblivious) cell-probe lower bound for ANN. This is the first super-logarithmic unconditional lower bound for ANN against general (non black-box) data structures. We also show that any oblivious static data structure for decomposable search problems (like ANN) can be obliviously dynamized with O(lg n) overhead in update and query time, strengthening a classic result of Bentley and Saxe (Algorithmica, 1980).

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/YCV3CBN4)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Tal Malkin\|Tal Malkin]], [[people/Omri Weinstein\|Omri Weinstein]], [[people/Kevin Yeo\|Kevin Yeo]], 
> Related:: 
> url:: https://epubs.siam.org/doi/10.1137/1.9781611975994.68
> doi:: 
> bibliography:: Larsen, Kasper Green, Tal Malkin, Omri Weinstein, and Kevin Yeo. 2019. “Lower Bounds for Oblivious Near-Neighbor Search.” In _Proceedings of the 2020 ACM-SIAM Symposium on Discrete Algorithms (SODA)_, 1116–34. Proceedings. Society for Industrial and Applied Mathematics. [https://doi.org/10.1137/1.9781611975994.68](https://doi.org/10.1137/1.9781611975994.68).

---
## My Notes


model:: Dynamic oblivious cell probe model 
techniques:: [[Techniques/Dynamic/Chronogram + Cell sampling\|Chronogram + Cell sampling]] 
problems::  statistically oblivious Approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] over $d$ dimesnional Hamming cube 
lbs:: $\Omega(d \lg n/(\lg \lg n)^2)$

The Lower bounds are in the Dynamic Oblivious Cell Probe Model, introuduced by Larsen and  Neilsen [[larsenYesThereIs2018]]




