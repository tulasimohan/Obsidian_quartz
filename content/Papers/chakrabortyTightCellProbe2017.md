---
{"publish":true,"title":"Tight cell probe bounds for succinct Boolean matrix-vector multiplication","created":"2025-05-24T17:36:28.135+01:00","modified":"2025-07-07T23:39:58.542+01:00","published":"2025-07-07T23:39:58.542+01:00","cssclasses":""}
---


# Tight cell probe bounds for succinct Boolean matrix-vector multiplication


>[!meta]- Abstract
The conjectured hardness of Boolean matrix-vector multiplication has been used with great success to prove conditional lower bounds for numerous important data structure problems, see Henzinger et al. [STOC’15]. 
In recent work, Larsen and Williams [SODA’17] attacked the problem from the upper bound side and gave a surprising cell probe data structure (that is, we only charge for memory accesses, while computation is free). 
Their cell probe data structure answers queries in Õ(n7/4) time and is succinct in the sense that it stores the input matrix in read-only memory, plus an additional Õ(n7/4) bits on the side. 
In this paper, we essentially settle the cell probe complexity of succinct Boolean matrix-vector multiplication. We present a new cell probe data structure with query time Õ(n3/2) storing just Õ(n3/2) bits on the side. We then complement our data structure with a lower bound showing that any data structure storing r bits on the side, with n ¡ r ¡ n2 must have query time t satisfying t r = Ω(n3). For r ≤ n, any data structure must have t = Ω(n2). Since lower bounds in the cell probe model also apply to classic word-RAM data structures, the lower bounds naturally carry over. We also prove similar lower bounds for matrix-vector multiplication over F2.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Diptarka Chakraborty\|Diptarka Chakraborty]], [[people/Lior Kamma\|Lior Kamma]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Chakraborty, Diptarka, Lior Kamma, and Kasper Green Larsen. 2017. ‘Tight Cell Probe Bounds for Succinct Boolean Matrix-Vector Multiplication’. [https://doi.org/10.1145/3188745.3188830](https://doi.org/10.1145/3188745.3188830).

---
## My Notes


problems::succint [[Problems/Data_Structures/Static/Matrix vector multiplication]]   
techniques:: restricted 
lbs:: 
Model:: Static
InorOut:: In

- [ ] to Read 




