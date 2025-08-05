---
{"publish":true,"title":"Lower bounds for online integer multiplication and convolution in the cell-probe model","created":"2025-05-24T17:36:27.212+01:00","modified":"2025-07-07T14:31:55.450+01:00","published":"2025-07-07T14:31:55.450+01:00","cssclasses":""}
---


# Lower bounds for online integer multiplication and convolution in the cell-probe model


>[!meta]- Abstract
We show time lower bounds for both **online integer multiplication** and convolution in the cell-probe model with word size _w_. 
>- For the multiplication problem, one pair of digits, each from one of two _n_ digit numbers that are to be multiplied, is given as input at step _i_. 
The online algorithm outputs a single new digit from the product of the numbers before step _i_ + 1. 
We give a lower bound of $Ω(δwlog⁡n)$ time on average per output digit for this problem where 2_δ_ is the maximum value of a digit. 
>- In the **convolution problem**, we are given a fixed vector _V_ of length _n_ and we consider a stream in which numbers arrive one at a time. We output the inner product of _V_ and the vector that consists of the last _n_ numbers of the stream. 
>We show an $Ω(δwlog⁡n)$ lower bound for the time required per new number in the stream. All the bounds presented hold under randomisation and amortisation. 
>Multiplication and convolution are central problems in the study of algorithms which also have the widest range of practical applications.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/R. Clifford\|R. Clifford]], [[people/Markus Jalsenius\|Markus Jalsenius]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Clifford, R., and Markus Jalsenius. 2011. ‘Lower Bounds for Online Integer Multiplication and Convolution in the Cell-Probe Model’. [https://doi.org/10.1007/978-3-642-22006-7_50](https://doi.org/10.1007/978-3-642-22006-7_50).

---
## My Notes


problems:: streaming problems[[Integer multiplication]] , [[Convolution]]
techniques::
Model:: streaming
lbs:: streaming lower-bounds
InorOut:: Out





