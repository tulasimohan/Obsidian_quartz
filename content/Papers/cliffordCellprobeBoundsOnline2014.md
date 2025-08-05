---
{"publish":true,"title":"Cell-probe bounds for online edit distance and other pattern matching problems","created":"2025-05-24T17:36:27.412+01:00","modified":"2025-07-07T14:31:55.454+01:00","published":"2025-07-07T14:31:55.454+01:00","cssclasses":""}
---


# Cell-probe bounds for online edit distance and other pattern matching problems


>[!meta]- Abstract
We give cell-probe bounds for the computation of edit distance, Hamming distance, convolution and longest common subsequence in a stream. 
In this model, a fixed string of n symbols is given and one δ-bit symbol arrives at a time in a stream. After each symbol arrives, the distance between the fixed string and a suffix of most recent symbols of the stream is reported. 
The cell-probe model is perhaps the strongest model of computation for showing data structure lower bounds, subsuming in particular the popular word-RAM model. 
• We first give an Ω((δ log n)/(w+log log n)) lower bound for the time to give each output for both online Hamming distance and convolution, where w is the word size. This bound relies on a new encoding scheme and for the first time holds even when w is as small as a single bit. 
• We then consider the online edit distance and longest common subsequence problems in the bit-probe model (w = 1) with a constant sized input alphabet. 
We give a lower bound of Ω([EQUATION]log n/(log log n)3/2) which applies for both problems. This second set of results relies both on our new encoding scheme as well as a carefully constructed hard input distribution. 
• Finally, for the online edit distance problem we show that there is an O((log2n)/w) upper bound in the cell-probe model. This bound gives a contrast to our new lower bound and also establishes an exponential gap between the known cell-probe and RAM model complexities.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/R. Clifford\|R. Clifford]], [[people/Markus Jalsenius\|Markus Jalsenius]], [[people/Benjamin Sach\|Benjamin Sach]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Clifford, R., Markus Jalsenius, and Benjamin Sach. 2014. ‘Cell-Probe Bounds for Online Edit Distance and Other Pattern Matching Problems’. [https://doi.org/10.1137/1.9781611973730.37](https://doi.org/10.1137/1.9781611973730.37).

---
## My Notes


Model:: Streaming
techniques::  
problems: Edit distance, Hamming distance
lbs::
InorOut:: Out




