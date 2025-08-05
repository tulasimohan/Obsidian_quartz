---
{"publish":true,"title":"The cell probe complexity of succinct data structures","created":"2025-05-24T17:36:28.114+01:00","modified":"2025-07-07T14:33:55.249+01:00","published":"2025-07-07T14:33:55.249+01:00","cssclasses":""}
---


# The cell probe complexity of succinct data structures


>[!meta]- Abstract
We consider time-space tradeoffs for static data structure problems in the cell probe model with word size 1 (the bit probe model). 
In this model, the goal is to represent n-bit data with s=n+r bits such that queries (of a certain type) about the data can be answered by reading at most t bits of the representation. I
deally, we would like to keep both s and t small, but there are tradeoffs between the values of s and t that limit the possibilities of keeping both parameters small. 
In this paper, we consider the case of succinct representations, where s=n+r for some redundancy r≪n. 
For a Boolean version of the problem of polynomial evaluation with preprocessing of coefficients, we show a lower bound on the redundancy–query time tradeoff of the form (r+1)t≥Ω(n/logn). 
In particular, for very small redundancies r, we get an almost optimal lower bound stating that the query algorithm has to inspect almost the entire data structure (up to a logarithmic factor). 
We show similar lower bounds for problems satisfying a certain combinatorial properties of a coding theoretic flavor, and obtain (r+1)t≥Ω(n) for certain problems. Previously, no ω(m) lower bounds were known on t in the general model for explicit Boolean problems, even for very small redundancies. By restricting our attention to systematic or index structures ϕ satisfying ϕ(x)=x⋅ϕ∗(x) for some map ϕ∗ (where ⋅ denotes concatenation), we show similar lower bounds on the redundancy–query time tradeoff for the natural data structuring problems of Prefix Sum and Substring Search.

> [!meta]- Metadata
> zotero_link:: [Full Text](zotero://select/groups/5902932/items/7QSVZN7M)
> Authors:: [[people/Anna Gál\|Anna Gál]], [[people/Peter Bro Miltersen\|Peter Bro Miltersen]], 
> Related:: 
> url:: https://www.sciencedirect.com/science/article/pii/S030439750700151X
> doi:: 
> bibliography:: Gál, Anna, and Peter Bro Miltersen. 2007. ‘The Cell Probe Complexity of Succinct Data Structures’. _Theoretical Computer Science_, Automata, Languages and Programming, 379 (3): 405–17. [https://doi.org/10.1016/j.tcs.2007.02.047](https://doi.org/10.1016/j.tcs.2007.02.047).

---
## My Notes


Model:: bit probe, Static  
problems:: [[../../Problems/Data_Structures/Both/Polynomial Evaluation\|Polynomial Evaluation]], [[Substring search]], [[Prefix sum]], [[Problems/Communication_Complexity/Membership]]
techniques::  
lbs:: 
InorOut:: In




