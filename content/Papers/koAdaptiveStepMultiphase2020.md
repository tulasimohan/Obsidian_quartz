---
{"publish":true,"title":"An Adaptive Step Toward the Multiphase Conjecture","created":"2025-07-07T16:57:15.683+01:00","modified":"2025-07-07T17:06:10.604+01:00","published":"2025-07-07T17:06:10.604+01:00","cssclasses":""}
---

# An Adaptive Step Toward the Multiphase Conjecture

>[!meta]- Abstract
In 2010, Pătraşcu proposed a dynamic set-disjointness problem, known as the [[Problems/Data_Structures/Dynamic/Multiphase problem\|Multiphase problem]], as a candidate for proving polynomial lower bounds on the operational time of dynamic data structures. 
He conjectured that any data structure for the Multiphase problem must make $n^{\epsilon}$ cell-probes in either update or query phases, and showed that this would imply similar unconditional lower bounds on many important dynamic data structure problems. There has been almost no progress on this conjecture in the past decade since its introduction. 
We show an $\tilde\Omega(\sqrt n)$ cell-probe lower bound on the Multiphase problem for data structures with general (adaptive) updates, and queries with unbounded but “layered” adaptivity. 
This result captures all known set-intersection data structures and significantly strengthens previous Multiphase lower bounds, which only captured non-adaptive data structures. 
Our main technical result is a communication lower bound on a 4-party variant of Pătraşcu's Number-On-Forehead Multiphase game, using information complexity techniques. 
We then use this result to make progress on understanding the power of nonlinear gates in networks computing linear operators, a long-standing open problem in circuit complexity and network design: 
We show that any depth-d circuit that computes a random $m\times n$ linear operator $x\mapsto Ax$ using gates of degree $k$ (width-$k$ DNFs) must have $\Omega(m\cdot n^1/2(d+k))$ wires. 
Finally, we show that a lower bound on Pătraşcu's original NOF game would imply a polynomial wire lower bound $(n^{1+\Omega(1/d)})$ for circuits with arbitrary gates computing a random linear operator. 
This suggests that the NOF conjecture is much stronger than its data structure counterpart.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/GMBBA9IK)
> Authors:: [[people/Young Kun Ko\|Young Kun Ko]], [[people/Omri Weinstein\|Omri Weinstein]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/document/9317945
> doi:: 
> bibliography:: Ko, Young Kun, and Omri Weinstein. 2020. “An Adaptive Step Toward the Multiphase Conjecture.” In _2020 IEEE 61st Annual Symposium on Foundations of Computer Science (FOCS)_, 752–61. [https://doi.org/10.1109/FOCS46700.2020.00075](https://doi.org/10.1109/FOCS46700.2020.00075).

---
## My Notes


model:: Dynamic adaptive updates and queries with layered adaptivity 
techniques:: [[4 Party Communication]] 4 party variant of [[Patrascu's NOF Multiphases game]]
problems:: [[Problems/Data_Structures/Dynamic/Multiphase problem\|Multiphase problem]]
lbs:: $\tilde{\Omega}(\sqrt{n})$ 




