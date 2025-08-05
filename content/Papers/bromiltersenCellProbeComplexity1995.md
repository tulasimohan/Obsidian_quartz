---
{"publish":true,"title":"On the cell probe complexity of polynomial evaluation","created":"2025-05-24T17:36:29.241+01:00","modified":"2025-07-11T13:17:23.394+01:00","published":"2025-07-11T13:17:23.394+01:00","cssclasses":""}
---


# On the cell probe complexity of polynomial evaluation


>[!meta]- Abstract
We consider the cell probe complexity of the polynomial evaluation problem with preprocessing of coefficients, for polynomials of degree at most $n$ over a finite field $K$. We show that the trivial cell probe algorithm for the problem is optimal if $K$ is sufficiently large compared to $n$. 
As an application, we give a new proof of the fact that $P ≠ incr-TIME(o(\log n/\log \log n))$.

> [!meta]- Metadata
> zotero_link:: [1-s2.0-0304397595800325-main](zotero://select/library/items/UZNAF4AT)
> Authors:: [[people/Peter Bro Miltersen\|Peter Bro Miltersen]], 
> Related:: 
> url:: https://www.sciencedirect.com/science/article/pii/0304397595800325
> doi:: 
> bibliography:: Bro Miltersen, Peter. 1995. ‘On the Cell Probe Complexity of Polynomial Evaluation’. _Theoretical Computer Science_ 143 (1): 167–74. [https://doi.org/10.1016/0304-3975(95)80032-5](https://doi.org/10.1016/0304-3975(95)80032-5).


---
## Self Notes



Parameters: 
- $|\mathbb{F}|$ = field size
- n = degree of the polynomial
- s = space used by the DS
- t = query complexity 

Techniques:: [[Techniques/Static/Richness\|Richness]]
Model:: Static
problems:: [[../../Problems/Data_Structures/Both/Polynomial Evaluation\|Polynomial Evaluation]]
lbs:: $t = \Omega(\frac{\log |\mathbb{F}| - \log n}{\log s})$



## Reading notes



  
_Imported: 2025-01-19 01:47_

### Upper and Lowerbounds

Highlight ([page.4](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The proof, which is not difficult,uses the technique of reduction from communication problems (first used implicitly by Ajtai [I], made explicit by Miltersen [8,9]) >  



