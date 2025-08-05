---
{"publish":true,"title":"Lower bounds for Union-Split-Find related problems on random access machines","created":"2025-05-24T17:36:26.046+01:00","modified":"2025-07-07T14:33:55.246+01:00","published":"2025-07-07T14:33:55.246+01:00","cssclasses":""}
---


# Lower bounds for Union-Split-Find related problems on random access machines


>[!meta]- Abstract
>We prove $Ω(\sqrt{\log \log n})$ lower bounds on the random access machine complexity of several dynamic, partially dynamic and static data structure problems, including the 
>- Union-Split-Find problem, 
>- dynamic prefix problems and 
>- one-dimensional range query problems. 
>
>The proof techniques include a general technique using perfect hashing for reducing static data structure problems (with a restriction of the size of the structure) into partially dynamic data structure problems (with no such restriction), thus providing a way to transfer lower bounds. 
>
>We use a generalization of a method due to Ajtai for proving the lower bounds on the static problems, but describe the proof in terms of communication complexity, revealing a striking similarity to the proof used by Karchmer and Wigderson for proving lower bounds on the monotone circuit depth of connectivity.




> [!meta]- Metadata
> zotero_link:: [Full Text](zotero://select/library/items/F7MA29CM)
> Authors:: [[people/Peter Bro Miltersen\|Peter Bro Miltersen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Miltersen, Peter Bro. 1994. ‘Lower Bounds for Union-Split-Find Related Problems on Random Access Machines’. In _Proc. 26th ACM Symposium on Theory of Computing (STOC)_, 625–34.


---
## Self Notes

Took Ajtai's technique and made it explicit as a communication lower bound. 

Techniques::  Ajtai's technique in communication language, reduction from static to dynamic using hashing
problems:: [[Problems/Data_Structures/Dynamic/Union-Split-Find]] , Dynamic Prefixes, [[../../1_Problems/Data_Structures/Both/Range Queries/1D Range Queries\|1D Range Queries]]
Model:: Static and Dynamic
lbs:: $\Omega(\sqrt{\log \log n})$



## Reading notes



  
_Imported: 2025-01-19 01:41_

### Lemmas

Note ([page.625](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> The Union-Split-Find problem (on intervals)  is the task of implementing a data type  UNION-SPLIT-FIND(n) containing a set S G  [n] = {1 . . . . . n}, initially empty, with the following operations:  l  l  l  For each i E [n] an operation Unio%. It removes i from S.  For each i E [n], an operation spliti. It inserts i into S.  For each i c [n], an operation f ind~. It returns the largest element of S which is smaller  than or equal to i if such an element exists,  otherwise O is returned. >

Highlight ([page.625](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> UNION-SPLIT-FIND(n) >  



