---
{"publish":true,"title":"Simple Average-Case Lower Bounds for Approximate Near-Neighbor from Isoperimetric Inequalities","created":"2025-07-07T15:45:45.172+01:00","modified":"2025-07-11T13:21:40.166+01:00","published":"2025-07-11T13:21:40.166+01:00","cssclasses":""}
---

# Simple Average-Case Lower Bounds for Approximate Near-Neighbor from Isoperimetric Inequalities

>[!meta]- Abstract
We prove an $\Omega(d/log(sw/nd))$ lower bound for the average-case cell-probe complexity of deterministic or Las Vegas randomized algorithms solving approximate near-neighbor (ANN) problem in ddimensional Hamming space in the cell-probe model with w-bit cells, using a table of size s. This lower bound matches the highest known worst-case cell-probe lower bounds for any static data structure problems.

This average-case cell-probe lower bound is proved in a general framework which relates the cell-probe complexity of ANN to isoperimetric inequalities in the underlying metric space. A tighter connection between ANN lower bounds and isoperimetric inequalities is established by a stronger richness lemma proved by cell-sampling techniques.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Yitong Yin\|Yitong Yin]], 
> Related:: 
> url:: https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ICALP.2016.84
> doi:: 
> bibliography:: Yin, Yitong. 2016. “Simple Average-Case Lower Bounds for Approximate Near-Neighbor from Isoperimetric Inequalities.” In _43rd International Colloquium on Automata, Languages, and Programming (ICALP 2016)_, edited by Ioannis Chatzigiannakis, Michael Mitzenmacher, Yuval Rabani, and Davide Sangiorgi, 55:84:1-84:13. Leibniz International Proceedings in Informatics (LIPIcs). Dagstuhl, Germany: Schloss Dagstuhl – Leibniz-Zentrum für Informatik. [https://doi.org/10.4230/LIPIcs.ICALP.2016.84](https://doi.org/10.4230/LIPIcs.ICALP.2016.84).

---
## My Notes


model:: Static 
techniques:: Stronger [[Techniques/Static/Richness\|Richness]] using cell sampling, Isoperimetric inequalities
problems:: Approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#Approximate Nearest Neighbour\|Nearest Neighbour]]
lbs::  $\Omega(d/\log(sw/nd))$ lower bound for the average-case cell-probe complexity of deterministic or Las Vegas randomized algorithms

Similar to the paper, that I discussed with Bruno on Nearest neighbour using Isoperimetric inequalities.  




