---
{"publish":true,"title":"Crossing the logarithmic barrier for dynamic Boolean data structure lower bounds","created":"2025-05-24T17:36:29.441+01:00","modified":"2025-07-08T20:03:18.363+01:00","published":"2025-07-08T20:03:18.363+01:00","cssclasses":""}
---


# Crossing the logarithmic barrier for dynamic Boolean data structure lower bounds


>[!meta]- Abstract
This paper proves the first super-logarithmic lower bounds on the cell probe complexity of dynamic boolean (a.k.a. decision) data structure problems, a long-standing milestone in data structure lower bounds. 
We introduce a new approach and use it to prove a $\Omega(\log^{1.5} n)$ lower bound on the operational time of a wide range of boolean data structure problems, most notably, on the query time of dynamic range counting over $\mathbb{F}_2$. 
Proving an $ω(\log n)$ lower bound for this problem was explicitly posed as one of five important open problems in the late Mihai Pǎtraşcu’s obituary&nbsp;. This result also implies the first $ω(\log n)$ lower bound for the classical 2D range counting problem, one of the most fundamental data structure problems in computational geometry and spatial databases. We derive similar lower bounds for boolean versions of dynamic polynomial evaluation and 2D rectangle stabbing, and for the (non-boolean) problems of range selection and range median. Our technical centerpiece is a new way of “weakly” simulating dynamic data structures using efficient one-way communication protocols with small advantage over random guessing. This simulation involves a surprising excursion to low-degree (Chebyshev) polynomials which may be of independent interest, and offers an entirely new algorithmic angle on the “cell sampling” method of Panigrahy et al.&nbsp;.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/J8YDXQ3M)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Omri Weinstein\|Omri Weinstein]], [[people/Huacheng Yu\|Huacheng Yu]], 
> Related:: [[Range selection and median: Tight cell probe lower bounds and adaptive data structures]], [[Logarithmic Lower Bounds in the Cell-Probe Model]], [[Tight bounds for the partial-sums problem]], [[Concrete mathematics: a foundation for computer science]], [[Range searching]], [[Should tables be sorted?]], [[Lower bounds for 2-dimensional range counting]], [[Space-efficient and fast algorithms for multidimensional dominance reporting and counting]], [[Models and techniques for proving data structure lower bounds]], [[The cell probe complexity of succinct data structures]], [[Mihai Pˇatras ̧cu: Obituary and open problems]], [[Fast Modular Composition in any Characteristic]], [[Cell-probe proofs]], [[Towards optimal range medians]], [[Pseudorandomness]], [[Bounds for small-error and zero-error quantum algorithms]], 
> url:: https://dl.acm.org/doi/10.1145/3188745.3188790
> doi:: 
> bibliography:: Larsen, Kasper Green, Omri Weinstein, and Huacheng Yu. 2018. ‘Crossing the Logarithmic Barrier for Dynamic Boolean Data Structure Lower Bounds’. In _Proceedings of the 50th Annual ACM SIGACT Symposium on Theory of Computing_, 978–89. STOC 2018. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/3188745.3188790](https://doi.org/10.1145/3188745.3188790).


---
## Self Notes


Model:: Dynamic
Techniques:: [[Techniques/Dynamic/chronogram + cell sampling + Peak to average]]
problems:: [[Problems/Data_Structures/Both/Range_Queries/Range Counting\|Range Counting]] over $\mathbb{F}_2$, [[Problems/Data_Structures/Both/Range_Queries/2D Range Reporting\|2D Range Reporting]] , [[Problems/Data_Structures/Both/Stabbing_Queries/2D Rectangle Stabbing]] , [[Problems/Data_Structures/Both/Range_Queries/Range Median\|Range Median]] 
lbs:: $\tilde\Omega(\log^{1.5} n)$








## Reading notes



  



