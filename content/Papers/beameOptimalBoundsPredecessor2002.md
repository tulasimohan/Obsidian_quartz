---
{"publish":true,"title":"Optimal bounds for the predecessor problem and related problems","created":"2025-05-24T17:36:27.287+01:00","modified":"2025-07-07T14:58:36.677+01:00","published":"2025-07-07T14:58:36.677+01:00","cssclasses":""}
---


# Optimal bounds for the predecessor problem and related problems


>[!meta]- Abstract
We obtain matching upper and lower bounds for the amount of time to find the predecessor of a given element among the elements of a fixed compactly stored set. Our algorithms are for the unit-cost word RAM with multiplication and are extended to give dynamic algorithms. The lower bounds are proved for a large class of problems, including both static and dynamic predecessor problems, in a much stronger communication game model, but they apply to the cell probe and RAM models.

> [!meta]- Metadata
> zotero_link:: [ScienceDirect Full Text PDF](zotero://select/groups/5902932/items/XIGQ5Q2P)
> Authors:: [[people/Paul Beame\|Paul Beame]], [[people/Faith E. Fich\|Faith E. Fich]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Beame, Paul, and Faith E. Fich. 2002. ‘Optimal Bounds for the Predecessor Problem and Related Problems’. _Journal of Computer and System Sciences_ 65 (1): 38–72. [https://doi.org/10.1006/jcss.2002.1822](https://doi.org/10.1006/jcss.2002.1822).


---
## Self Notes


Parameters:: $U = [n]$ and $A \subseteq U$, $|A|=m$ 

Techniques:: Ajtai's technique on a different distribution.
Model:: Static and Dynamic
problems:: [[Problems/Data_Structures/Both/Predecessor\|Predecessor]] , [[Problems/Data_Structures/Static/Prefix Parity\|Prefix Parity]] , [[Problems/Data_Structures/Static/Point Seperation\|Point seperation]] , [[Problems/Data_Structures/Static/Rank\|Rank]] problem, [[Problems/Data_Structures/Both/Range_Queries/Range Counting\|Range Counting]]
lbs:: 
  - Static Predecessor: $Ω(\frac{\log \log n}{\log \log \log n})$ in cell probe and RAM models.
  - Dynamic Predecessor: $Ω(\frac{\log \log n}{\log \log \log n}\log \log m)$ in cell probe model.

Predecessor reduces to [[Problems/Data_Structures/Static/Prefix Parity\|Prefix Parity]] , [[Problems/Data_Structures/Static/Point Seperation\|Point seperation]] , [[Problems/Data_Structures/Static/Rank\|Rank]] problem, [[../../Problems/Data_Structures/Both/Range Queries/Range Counting\|Range Counting]]. 



## Reading notes



  
_Imported: 2025-03-14 12:49_

### Theorems and Corollaries

Note ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> - **reduction dynamic to static**  
>

### Lemmas

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> static predecessor >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> dynamic predecessor >

### Upper and Lowerbounds

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> matching upper and lower bounds >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Predecessor queries >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> nearest neighbour queries >

Note ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> rank >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> van Emde Boas trees [42, 43] can be used to perform predecessor queries on any set of integers from a universe of size N in O(log log N) time, but they require W(N) space >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> two level perfect hashing >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Fusion trees >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> generic transformations of Andersson and Thorup >  



