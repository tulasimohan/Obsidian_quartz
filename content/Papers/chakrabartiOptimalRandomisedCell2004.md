---
{"publish":true,"title":"An optimal randomised cell probe lower bound for approximate nearest neighbour searching","created":"2025-05-24T17:36:27.575+01:00","modified":"2025-07-11T13:26:20.322+01:00","published":"2025-07-11T13:26:20.322+01:00","cssclasses":""}
---


# An optimal randomised cell probe lower bound for approximate nearest neighbour searching


>[!meta]- Abstract
We consider the approximate nearest neighbour search problem on the Hamming cube {0, 1 }/sup d/. 
We show that a randomised cell probe algorithm that uses polynomial storage and word size d/sup O(1)/ requires a worst case query time of  $\Omega/ (\log \log d/ \log \log \log d)$. The approximation factor may be as loose as 2/sup log 1 - /spl eta//d for any fixed /spl eta/ ¿ 0. This generalises an earlier result (Chakrabarti et al., 1999) on the deterministic complexity of the same problem and, more importantly, fills a major gap in the study of this problem since all earlier lower bounds either did not allow randomisation according to Chakrabarti et al. (1999) and Liu (2003) or did not allow approximation according to Borodin et al. (1999), Barkol and Rabani (2000), and Jayram et al. (2003). We also give a cell probe algorithm which proves that our lower bound is optimal. Our proof uses a lower bound on the round complexity of the related communication problem. We show, additionally, that considerations of bit complexity alone cannot prove any nontrivial cell probe lower bound for the problem. This shows that the richness technique (Miltersen et al., 1995) used in a lot of research around this problem would not have helped here. Our proof is based on information theoretic techniques for communication complexity, a theme that has been prominent in research by Chakrabarti et al. (2001), Bar-Yossef et al. (2002), Sen (2003) and Jain et al. (2003). In particular, we make heavy use of the round elimination and message compression ideas in the work of Sen (2003) and Jain et al. (2003), and also introduce a technique which we call message switching.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Amit Chakrabarti\|Amit Chakrabarti]], [[people/O. Regev\|O. Regev]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Chakrabarti, Amit, and O. Regev. 2004. ‘An Optimal Randomised Cell Probe Lower Bound for Approximate Nearest Neighbour Searching’. [https://doi.org/10.1109/FOCS.2004.12](https://doi.org/10.1109/FOCS.2004.12).

---
## My Notes


Model:: Static
techniques:: [[Techniques/Static/Round elimination\|Round elimination]] and message compression, message switching 
problems:: approximate [[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour\|Nearest Neighbour]] search on hamming cube,
lbs:: $\Omega/ (\log \log d/ \log \log \log d)$
InorOut:: Out

Randomized lower-bound

Earlier lower-bounds did not allow randomness Chakrabarti et al. (1999) and Liu (2003) or did not allow approximation according to Borodin et al. (1999), Barkol and Rabani (2000), and Jayram et al. (2003). 

In particular, we make heavy use of the round elimination and message compression ideas in the work of Sen (2003) and Jain et al. (2003)



