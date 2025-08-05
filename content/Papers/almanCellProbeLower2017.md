---
{"publish":true,"title":"Cell-probe lower bounds from online communication complexity","created":"2025-05-24T17:36:28.792+01:00","modified":"2025-07-07T14:31:55.453+01:00","published":"2025-07-07T14:31:55.453+01:00","cssclasses":""}
---


# Cell-probe lower bounds from online communication complexity


>[!meta]- Abstract
In this work, ==we introduce an online model for communication complexity==. 
Analogous to how online algorithms receive their input piece-by-piece, our model presents one of the players, Bob, his input piece-by-piece, and has the players Alice and Bob cooperate to compute a result each time before the next piece is revealed to Bob. 
This model has a closer and more natural correspondence to dynamic data structures than classic communication models do, and hence presents a new perspective on data structures. 
We first present a tight lower bound for the online set intersection problem in the online communication model, demonstrating a general approach for proving online communication lower bounds. 
The online communication model prevents a batching trick that classic communication complexity allows, and yields a stronger lower bound. We then apply the online communication model to prove data structure lower bounds for two dynamic data structure problems: the Group Range problem and the Dynamic Connectivity problem for forests. Both of the problems admit a worst case O(logn)-time data structure. Using online communication complexity, we prove a tight cell-probe lower bound for each: spending o(logn) (even amortized) time per operation results in at best an exp(−δ2 n) probability of correctly answering a (1/2+δ)-fraction of the n queries.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Josh Alman\|Josh Alman]], [[people/Joshua R. Wang\|Joshua R. Wang]], [[people/Huacheng Yu\|Huacheng Yu]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Alman, Josh, Joshua R. Wang, and Huacheng Yu. 2017. ‘Cell-Probe Lower Bounds from Online Communication Complexity’. [https://doi.org/10.1145/3188745.3188862](https://doi.org/10.1145/3188745.3188862).

---
## My Notes


Model:: Online Communication  
Problems::  Online [[Set Intersection]], [[Group Range]], [[Problems/Data_Structures/Dynamic/Connectivity#^e48c5b\|Dynamic Connectivity for forests]] 
Techniques::Online communication complexity reductions  
lbs::$Ω(\log n)$ time per operation required for high correctness probability
InorOut : Out
to read:: Yes

Online communication model, not standard Dynamic model. 





