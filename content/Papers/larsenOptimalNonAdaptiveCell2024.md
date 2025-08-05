---
{"publish":true,"title":"Optimal Non-Adaptive Cell Probe Dictionaries and Hashing","created":"2025-05-25T01:31:06.512+01:00","modified":"2025-07-07T22:17:52.138+01:00","published":"2025-07-07T22:17:52.138+01:00","cssclasses":""}
---


# Optimal Non-Adaptive Cell Probe Dictionaries and Hashing


>[!meta]- Abstract
We present a simple and provably optimal non-adaptive cell probe data structure for the static [[Problems/Data_Structures/Static/Dictionary\|Dictionary]] problem.
Our data structure supports storing a set of $n$ key-value pairs from $[u] \times [u]$ using $s$ words of space and answering key lookup queries in $t = O(\log(u/n)/ \log(s/n))$ non-adaptive probes. 
This generalizes a solution to the membership problem (i.e., where no values are associated with keys) due to Buhrman et al. 
We also present matching lower bounds for the non-adaptive static membership problem in the deterministic setting. 
Our lower bound implies that both our dictionary algorithm and the preceding membership algorithm are optimal, and in particular that there is an inherent complexity gap in these problems between no adaptivity and one round of adaptivity (with which hashing-based algorithms solve these problems in constant time).

> [!meta]- Metadata
> zotero_link:: [PDF](zotero://select/groups/5902932/items/6IYFUZUK)
> Authors:: [[people/Kasper Green Larsen\|Kasper Green Larsen]], [[people/Rasmus Pagh\|Rasmus Pagh]], [[people/Giuseppe Persiano\|Giuseppe Persiano]], [[people/Toniann Pitassi\|Toniann Pitassi]], [[people/Kevin Yeo\|Kevin Yeo]], [[people/Or Zamir\|Or Zamir]], 
> Related:: 
> url:: https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ICALP.2024.104
> doi:: 
> bibliography:: Larsen, Kasper Green, Rasmus Pagh, Giuseppe Persiano, Toniann Pitassi, Kevin Yeo, and Or Zamir. 2024. ‘Optimal Non-Adaptive Cell Probe Dictionaries and Hashing’. Application/pdf. In _LIPIcs, Volume 297, ICALP 2024_, edited by Karl Bringmann, Martin Grohe, Gabriele Puppis, and Ola Svensson, 297:104:1-104:12. Schloss Dagstuhl – Leibniz-Zentrum für Informatik. [https://doi.org/10.4230/LIPICS.ICALP.2024.104](https://doi.org/10.4230/LIPICS.ICALP.2024.104).

---
## My Notes


model::Static, non-adaptive
techniques:: [[Techniques/Static/Cell Sampling\|Cell Sampling]]
problems:: [[Problems/Data_Structures/Static/Dictionary\|Dictionary]] , [[Problems/Communication_Complexity/Membership\|Membership]]
lbs:: 
notes:: non-adaptive lower bound



