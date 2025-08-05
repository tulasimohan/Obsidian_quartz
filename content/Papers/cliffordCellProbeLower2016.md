---
{"publish":true,"title":"Cell-probe lower bounds for bit stream computation","created":"2025-05-24T17:36:27.307+01:00","modified":"2025-07-07T14:31:55.455+01:00","published":"2025-07-07T14:31:55.455+01:00","cssclasses":""}
---


# Cell-probe lower bounds for bit stream computation


>[!meta]- Abstract
We revisit the complexity of online computation in the cell probe model. We consider a class of problems where we are first given a fixed pattern F of n symbols and then one symbol arrives at a time in a stream. After each symbol has arrived we must output some function of F and the n-length suffix of the arriving stream. Cell probe bounds of Omega(delta lg n/w) have previously been shown for both convolution and Hamming distance in this setting, where delta is the size of a symbol in bits and w in Omega(lg n) is the cell size in bits. However, when delta is a constant, as it is in many natural situations, the existing approaches no longer give us non-trivial bounds. We introduce a lop-sided information transfer proof technique which enables us to prove meaningful lower bounds even for constant size input alphabets. Our new framework is capable of proving amortised cell probe lower bounds of Omega(lg^2 n/(w lg lg n)) time per arriving bit. We demonstrate this technique by showing a new lower bound for a problem known as pattern matching with address errors or the L_2-rearrangement distance problem. This gives the first non-trivial cell probe lower bound for any online problem on bit streams that still holds when the cell size is large.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/R. Clifford\|R. Clifford]], [[people/Markus Jalsenius\|Markus Jalsenius]], [[people/Benjamin Sach\|Benjamin Sach]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Clifford, R., Markus Jalsenius, and Benjamin Sach. 2016. ‘Cell-Probe Lower Bounds for Bit Stream Computation’. [https://doi.org/10.4230/LIPIcs.ESA.2016.31](https://doi.org/10.4230/LIPIcs.ESA.2016.31).

---
## My Notes


Model:: streaming
problems::$\ell_2$-rearrangement distance problem
techniques:: lopsided information transfer
InorOut:: Out 

Streaming 

Our new framework is capable of proving amortised cell probe lower bounds of Omega(lg^2 n/(w lg lg n)) time per arriving bit



