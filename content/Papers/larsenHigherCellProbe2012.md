---
{"publish":true,"title":"Higher Cell Probe Lower Bounds for Evaluating Polynomials","created":"2025-05-24T17:36:27.942+01:00","modified":"2025-07-07T22:20:47.290+01:00","published":"2025-07-07T22:20:47.290+01:00","cssclasses":""}
---


# Higher Cell Probe Lower Bounds for Evaluating Polynomials

$\newcommand{\F}{\mathbb{F}}$
>[!meta]- Abstract
In this paper, we study the cell probe complexity of evaluating an $n$-degree polynomial $P$ over a finite field $\mathbb{F}$ of size at least $n^{1+\Omega(1)}$. 
More specifically, we show that any static data structure for evaluating $P(x)$, where $x \in \mathbb{F}$, must use $\omega(\log |\F|/ \log(Sw/n \log |\F|))$ cell probes to answer a query, where $S$ denotes the space of the data structure in number of cells and $w$ the cell size in bits. 
This bound holds in expectation for randomized data structures with any constant error probability $\delta < 1/2$. 
>- Our lower bound not only improves over the $Ω(\log |\F|/ \log S)$ lower bound of Miltersen [TCS'95], but is in fact the highest static cell probe lower bound to date: For linear space (i.e. $S = O(n \log |\F|/w)$), our query time lower bound simplifies to $\Omega(lg |\F|)$, whereas the highest previous lower bound for any static data structure problem having d different queries is $\Omega(\log d/ \log \log d)$, which was first achieved by Pátrascu and Thorup [SICOMP'10]. 
>- We also use the recent technique of Larsen [STOC'12] to show a lower bound of $t_q = \Omega(\log |\F| \log n/\log(wt_u/ \log |\F|) \log(wt_u))$ for dynamic data structures for polynomial evaluation over a finite field $\F$ of size $\Omega(n^2)$. Here tq denotes the expected query time and tu the worst case update time. This lower bound holds for randomized data structures with any constant error probability $δ <; 1/2$. This is only the second time a lower bound beyond $\max t_u, tq = Ω(\max \log n, \log d/ \log \log d)$ has been achieved for dynamic data structures, where $d$ denotes the number of different queries and updates to the problem. Furthermore, it is the first such lower bound that holds for randomized data structures with a constant probability of error.


> [!meta]- Metadata
> zotero_link:: [IEEE Xplore Full Text PDF](zotero://select/library/items/5U4DDZF8)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: https://ieeexplore.ieee.org/document/6375307
> doi:: 
> bibliography:: Larsen, Kasper Green. 2012. ‘Higher Cell Probe Lower Bounds for Evaluating Polynomials’. In _2012 IEEE 53rd Annual Symposium on Foundations of Computer Science_, 293–301. [https://doi.org/10.1109/FOCS.2012.21](https://doi.org/10.1109/FOCS.2012.21).


---
## Self Notes


Model:: Static and Dynamic
problems::Static and Dynamic  [[Problems/Data_Structures/Polynomial Evaluation\|Polynomial Evaluation]]
Techniques:: [[Techniques/Dynamic/Chronogram + Cell sampling\|Chronogram + Cell sampling]] , [[Techniques/Static/Cell Sampling\|Cell Sampling]]
lbs::
- $t_q = \log \frac{|\F|}{ \log S}$ for Static
- $t_q = \Omega(\frac{\log |\F| \log n}{\log(wt_u/ \log |\F|) \log(wt_u)})$ for Dynamic



## Reading notes



  



