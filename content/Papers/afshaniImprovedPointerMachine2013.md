---
{"publish":true,"title":"Improved pointer machine and i/o lower bounds for simplex range reporting and related problems","created":"2025-05-24T17:36:29.743+01:00","modified":"2025-07-07T14:33:55.246+01:00","published":"2025-07-07T14:33:55.246+01:00","cssclasses":""}
---


# Improved pointer machine and i/o lower bounds for simplex range reporting and related problems


>[!meta]- Abstract
We investigate one of the fundamental areas in computational geometry: lower bounds for range reporting problems in the pointer machine and the external memory models. We develop new techniques that lead to new and improved lower bounds for simplex range reporting as well as some other geometric problems.
>- Simplex range reporting is the problem of storing n points in the $d$-dimensional space in a data structure such that the k points that lie inside a query simplex can be found efficiently. 
This is one of the fundamental and extensively studied problems in computational geometry. 
>- Currently, the best data structures for the problem achieve Q(n) + O(k) query time using space in which the  notation either hides a polylogarithmic or an nε factor for any constant ε > 0, (depending on the data structure and Q(n)). 
>- The best lower bound on this problem is due to Chazelle and Rosenberg who showed any pointer machine data structure that can answer queries in O(nγ + k) time must use Ω(nd-ε-dγ) space. Observe that this bound is a polynomial factor away from the best known data structures. In this article, we improve the space lower bound to . Not only this bridges the gap from polynomial to sub-polynomial, it also offers a smooth trade-off curve. For instance, for polylogarithmic values of Q(n), our space lower bound almost equals Ω((n/Q(n))d); the latter is generally believed to be the “right” bound. By a simple geometric transformation, we also improve the best lower bounds for the halfspace range reporting problem. Furthermore, we study the external memory model and offer a new simple framework for proving lower bounds in this model. We show that answering simplex range reporting queries with Q(n)+O(k/B) I/Os requires ) space or  blocks, in which B is the block size.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Peyman Afshani\|Peyman Afshani]], 
> Related:: 
> url:: https://www.worldscientific.com/doi/abs/10.1142/S0218195913600054
> doi:: 
> bibliography:: Afshani, Peyman. 2013. ‘Improved Pointer Machine and i/o Lower Bounds for Simplex Range Reporting and Related Problems’. _International Journal of Computational Geometry & Applications_ 23 (04n05): 233–51. [https://doi.org/10.1142/S0218195913600054](https://doi.org/10.1142/S0218195913600054).

---
## My Notes



Model::Static  
Problems:: [[../../1_Problems/Data_Structures/Both/Range Queries/Range Reporting#^7dc49f\|Simplex Range Reporting]] , [[../../1_Problems/Data_Structures/Both/Range Queries/Range Reporting#^e7eced\|Half-space Range Reporting]] 
Techniques::  not a cell probe lb
lbs::Space required $\Omega((𝑛/𝑄(𝑛))^𝑑 / 2^𝑂(√log 𝑄(𝑛)))$ for 𝑄(𝑛) + 𝑂(𝑘) query time
models:: pointer machine, external memory  
InorOut: Out

not cell probe

>[!SDSP] Simplex range reporting 
is the problem of storing n points in the d-dimensional space in a data structure such that the 
k points that lie inside a query simplex can be found efficiently.




