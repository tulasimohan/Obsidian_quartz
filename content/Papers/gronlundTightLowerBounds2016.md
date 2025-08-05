---
{"publish":true,"title":"Towards Tight Lower Bounds for Range Reporting on the RAM","created":"2025-05-24T17:36:25.966+01:00","modified":"2025-07-07T14:33:55.246+01:00","published":"2025-07-07T14:33:55.246+01:00","cssclasses":""}
---


# Towards Tight Lower Bounds for Range Reporting on the RAM

>[!meta]- Abstract
In the orthogonal range reporting problem, we are to preprocess a set of n points with integer coordinates on a UxU grid. The goal is to support reporting all k points inside an axis-aligned query rectangle. This is one of the most fundamental data structure problems in databases and computational geometry. Despite the importance of the problem its complexity remains unresolved in the word-RAM.

On the upper bound side, three best trade-offs exist, all derived by reducing range reporting to a ball-inheritance problem. Ball-inheritance is a problem that essentially encapsulates all previous attempts at solving range reporting in the word-RAM. In this paper we make progress towards closing the gap between the upper and lower bounds for range reporting by proving cell probe lower bounds for ball-inheritance. Our lower bounds are tight for a large range of parameters, excluding any further progress for range reporting using the ball-inheritance reduction.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/T88SDWG6)
> Authors:: [[people/Allan Grønlund\|Allan Grønlund]], [[people/Kasper Green Larsen\|Kasper Green Larsen]], 
> Related:: 
> url:: https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ICALP.2016.92
> doi:: 
> bibliography:: Grønlund, Allan, and Kasper Green Larsen. 2016. ‘Towards Tight Lower Bounds for Range Reporting on the RAM’. In _43rd International Colloquium on Automata, Languages, and Programming (ICALP 2016)_, 92:1-92:12. Schloss Dagstuhl – Leibniz-Zentrum für Informatik. [https://doi.org/10.4230/LIPIcs.ICALP.2016.92](https://doi.org/10.4230/LIPIcs.ICALP.2016.92).


---
## Self Notes


Techniques:: probe elimination + [[Papers/patrascuTimespaceTradeoffsPredecessor2006]] 
Model:: Static
Problems:: [[../../Problems/Data_Structures/Both/Range Queries/Orthogonal Range Reporting\|Orthogonal Range Reporting]] , [[Problems/Data_Structures/Static/Ball inheritance\|Ball inheritance]] problem
lbs::   
- Ω(log n) query time for k = 1.
- Ω(log n + k) query time for general k.

- Rank space reduction is explained. 
  For $(x,y)$, replace it by $(rk_x(x),rk_y(y))$ which is the rank among $x$-coordinates and $y$-coordinates respectively. 

#### Concepts
**published bits:** data structure is allowed to publish bits at preprocessing time that the query algorithm may read free of charge 
**accepted queries:** After inspecting a given query and the published bits, a data structure can choose to reject the query and not return an answer. Otherwise, the query is accepted and the algorithm must output the correct answer.  

- Probe elimination lemma







## Reading notes



  



