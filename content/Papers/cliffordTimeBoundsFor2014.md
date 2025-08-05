---
{"publish":true,"title":"Time bounds for streaming problems","created":"2025-05-24T17:36:26.013+01:00","modified":"2025-07-07T14:31:55.454+01:00","published":"2025-07-07T14:31:55.454+01:00","cssclasses":""}
---


# Time bounds for streaming problems


>[!meta]- Abstract
We give tight cell-probe bounds for the time to compute convolution, multiplication and Hamming distance in a stream. The cell probe model is a particularly strong computational model and subsumes, for example, the popular word RAM model. We first consider online convolution where the task is to output the inner product between a fixed n-dimensional vector and a vector of the n most recent values from a stream. One symbol of the stream arrives at a time and the each output must be computed before the next symbols arrives. Next we show bounds for online multiplication where the stream consists of pairs of digits, one from each of two n digit numbers that are to be multiplied. One pair arrives at a time and the task is to output a single new digit from the product before the next pair of digits arrives. Finally we look at the online Hamming distance problem where the Hamming distance is outputted instead of the inner product. For each of these three problems, we give a lower bound of Ω(<sup>{</sup>⁄<sub>δ</sub>}{w}n) time on average per output, where δ is the number of bits needed to represent an input symbol and w is the cell or word size. We argue that these bound are in fact tight within the cell probe model.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/R. Clifford\|R. Clifford]], [[people/Markus Jalsenius\|Markus Jalsenius]], [[people/Benjamin Sach\|Benjamin Sach]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Clifford, R., Markus Jalsenius, and Benjamin Sach. 2014. ‘Time Bounds for Streaming Problems’. [https://doi.org/10.4086/toc.2019.v015a002](https://doi.org/10.4086/toc.2019.v015a002).

---
## My Notes


Model:: streaming 




