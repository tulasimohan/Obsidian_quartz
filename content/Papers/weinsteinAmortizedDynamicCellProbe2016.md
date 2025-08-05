---
{"publish":true,"title":"Amortized Dynamic Cell-Probe Lower Bounds from Four-Party Communication","created":"2025-07-07T16:07:33.494+01:00","modified":"2025-07-07T21:30:33.354+01:00","published":"2025-07-07T21:30:33.354+01:00","cssclasses":""}
---

# Amortized Dynamic Cell-Probe Lower Bounds from Four-Party Communication

>[!meta]- Abstract
This paper develops a new technique for proving amortized, randomized cell-probe lower bounds on dynamic data structure problems. We introduce a new randomized nondeterministic four-party communication model that enables "accelerated", error-preserving simulations of dynamic data structures. We use this technique to prove an Ω(n(log n/log log n)2) cell-probe lower bound for the dynamic 2D weighted orthogonal range counting problem (2D-ORC) with n/poly log n updates and n queries, that holds even for data structures with exp(-Ω̃(n)) success probability. This result not only proves the highest amortized lower bound to date, but is also tight in the strongest possible sense, as a matching upper bound can be obtained by a deterministic data structure with worst-case operational time. This is the first demonstration of a "sharp threshold" phenomenon for dynamic data structures. Our broader motivation is that cell-probe lower bounds for exponentially small success facilitate reductions from dynamic to static data structures. As a proof-of-concept, we show that a slightly strengthened version of our lower bound would imply an Ω((log n/log log n)2) lower bound for the static 3D-ORC problem with O(n logO(1) n) space. Such result would give a near quadratic improvement over the highest known static cell-probe lower bound, and break the long standing Ω(log n) barrier for static data structures.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/6YXJ2PS4)
> Authors:: [[people/Omri Weinstein\|Omri Weinstein]], [[people/Huacheng Yu\|Huacheng Yu]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/document/7782944
> doi:: 
> bibliography:: Weinstein, Omri, and Huacheng Yu. 2016. “Amortized Dynamic Cell-Probe Lower Bounds from Four-Party Communication.” In _2016 IEEE 57th Annual Symposium on Foundations of Computer Science (FOCS)_, 305–14. [https://doi.org/10.1109/FOCS.2016.41](https://doi.org/10.1109/FOCS.2016.41).

---
## My Notes


model:: Dynamic
techniques:: Four-party communication
problems:: 3D [[Problems/Data_Structures/Both/Range_Queries/Orthogonal Range Counting\|ORC]]
lbs:: $\Omega(n (\log n/ \log \log n)^2)$ lower bound for $n/\mathrm{poly} \log n$ updates and $n$ queries that hold even for error $exp(-\tilde{\Omega }(n))$

- [ ] To Read




