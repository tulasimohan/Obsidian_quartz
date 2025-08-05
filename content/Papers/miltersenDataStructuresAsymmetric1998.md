---
{"publish":true,"title":"On Data Structures and Asymmetric Communication Complexity","created":"2025-05-24T17:36:28.607+01:00","modified":"2025-07-11T13:19:03.609+01:00","published":"2025-07-11T13:19:03.609+01:00","cssclasses":""}
---


# On Data Structures and Asymmetric Communication Complexity


>[!meta]- Abstract
In this paper we consider two-party communication complexity, the “asymmetric case”, when the input sizes of the two players differ significantly. Most of previous work on communication complexity only considers the total number of bits sent, but we study trade-offs between the number of bits the first player sends and the number of bits the second sends. These types of questions are closely related to the complexity of static data structure problems in the cell probe model. We derive two generally applicable methods of proving lower bounds and obtain several applications. These applications include new lower bounds for data structures in the cell probe model. Of particular interest is our “round elimination” lemma, which is interesting also for the usual symmetric communication case. This lemma generalizes and abstracts in a very clean form the “round reduction” techniques used in many previous lower bound proofs.

> [!meta]- Metadata
> zotero_link:: [ScienceDirect Full Text PDF](zotero://select/library/items/YD65GLEU)
> Authors:: [[people/Peter Bro Miltersen\|Peter Bro Miltersen]], [[people/Noam Nisan\|Noam Nisan]], [[people/Shmuel Safra\|Shmuel Safra]], [[people/Avi Wigderson\|Avi Wigderson]], 
> Related:: 
> url:: https://www.sciencedirect.com/science/article/pii/S002200009891577X
> doi:: 
> bibliography:: Miltersen, Peter Bro, Noam Nisan, Shmuel Safra, and Avi Wigderson. 1998. ‘On Data Structures and Asymmetric Communication Complexity’. _Journal of Computer and System Sciences_ 57 (1): 37–49. [https://doi.org/10.1006/jcss.1998.1577](https://doi.org/10.1006/jcss.1998.1577).


---
## Self Notes


>Notation:
>

Techniques::[[Techniques/Static/Round elimination\|Round elimination]], [[Techniques/Static/Richness\|Richness]]
problems:: [[Problems/Data_Structures/Static/Dictionary\|Dictionary]] , [[Problems/Data_Structures/Both/Predecessor\|Predecessor]], [[Problems/Data_Structures/Static/Prefix Parity\|Prefix Parity]], [[Problems/Communication_Complexity/Range Query\|Range Query]], [[Problems/Communication_Complexity/Membership\|Membership]], [[Problems/Communication_Complexity/Greater than\|Greater than]], [[Problems/Communication_Complexity/SetDisjointness\|SetDisjointness]] , [[Problems/Communication_Complexity/Span\|Span]]
Model:: Static
lbs:: 



## Reading notes



  
_Imported: 2025-01-19 01:46_

### Theorems and Corollaries

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> In a static data structure problem, we are given a domain D of possible data, a domain Q of possible queries, and a map f: Q_D A, where f(x, y) is the answer to query x about data y. >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> A solution with parameters s, b, and t is a method of storing any y # D as a data structure ,( y) in the memory of a random access machine, using s memory cells, each containing b bits, so that any query in Q can be answered by accessing at most t memory cells >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> An [a, b]-protocol for f is a protocol where the total number of bits that Alice sends Bob is at most a and the total number of bits that Bob sends Alice is at most b >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Alice gets m strings x1 , ..., xm and Bob gets a string y and an integer 1 i m. Their aim is to compute f (xi , y). >

Highlight ([page.47](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> pointer machine model >

Highlight ([page.47](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> layered partition model >

### Lemmas

Highlight ([page.37](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> MEMN, l >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> dictionary problem >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> disjointness problem >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> membership problem >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> span problem >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> new communication problem >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Pm( f ) >

Highlight ([page.40](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> partial match query >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> problem of storing a subset y U=[0, ..., 2n&1] so that for any x # U, the predecessor query ``What is max[z # y | z x]'' >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> prefix parity problem >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> communication problem PARn, l where Alice gets x # U, Bob gets y U of size at most l and the players must determine |[z # y | z x]| mod 2= | y & [0, x]| mod 2 >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> r-dimensional reporting range query problem >

Note ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Given a data set y U r, construct a static data structure using at most s memory cells, each containing b=O(n) bits, so that for any interval x=[x1 , x2] (for r=1) or box x=[x1 , x2]_ [z1, z2] (for r=2) we can answer the query ``What is x & y?'' efficiently. >

Highlight ([page.47](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> RQn, l >

Note ([page.47](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> where Alice gets an interval [x1 , x2], Bob gets a set y U of size at most l, and the players must agree on an element in [x1 , x2] & y if one exists >

### Claims and Propositions

Highlight ([page.37](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> rank technique >

Highlight ([page.37](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> large monochrome submatrix technique >

### Upper and Lowerbounds

Highlight ([page.37](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> round elimination'' lemma >

Highlight ([page.37](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> round reduction'' techniques >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> consider the communication problem, where Alice gets x # Q, Bob gets y # D, and they must determine f (x, y). For the dictionary problem, the corresponding communication problem is thus MEMN, l >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> If there is a solution to the data structure problem with parameters s, b, and t, then there is a protocol for the communication problem, with 2t rounds of communication, where Alice sends log s bits in each of her messages and Bob sends b bits in each of his messages >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> by a result in [Mil93], when the number of rounds of communication is not constant, for almost all data structure problems (with natural choices of parameters) the cell probe complexity is significantly (as much as exponentially) larger than the communication complexity >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> much better lower bounds imply time space trade-offs for branching programs >

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> If a function f: [0, 1]n_[0, 1]m [0, 1] can be computed by polynomial size, read O(1) times branching programs, then there is a data structure storing y # [0, 1]m using s=mO(1) cells each of size b log m so that any query x # [0, 1]n can be answered in t=O(n (log b&log log m)) probes. >

Highlight ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Richness Lemma. Let f be a (u, v)-rich problem. If f has a randomized one-sided error [a, b]-protocol, then f contains a submatrix of dimensions at least u 2a+2_v 2a+b+2 containing only 1-entries. >

Highlight ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Round Elimination Lemma. Let C=99 and R=4256.  Suppose there is a randomized [t, a, b]A-protocol for solving PRa( f ). Then there is a randomized [t&1, Ca, Cb]B-protocol for solving f. >

Image ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> “” could not be found.  
>

Image ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> “” could not be found.  
>

Image ([page.39](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> “” could not be found.  
>

Note ([page.40](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Theorem 3 [Mil93]. For a random data structure problem f: [0, 1]n_[0, 1]m [0, 1] the following holds with high probability: For any representation using s 2n&1 b cells of size b, query time 0(m b) is necessary. >

Highlight ([page.43](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Theorem 11. Let k l<N 2. If the disjointness problem has a randomized one-sided error [a, b]-protocol, then either a=0(k) or b=0(l ). Moreover, for a>k, b=0(l 2a k&a) >

Image ([page.43](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> “” could not be found.  
>

Note ([page.44](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Suppose there is a randomized [t, a, b]A-protocol with error probability $ for solving Pm( f ). Then there is a randomized [t&1, a, b]B-protocol with error probability = for solving f. >

Highlight ([page.45](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Lemma 14 (Round elimination lemma; fixed error probability). Let C=99 and R=4256. Suppose there is a randomized [t, a, b]A-protocol with error probability 1 3 for solving PRa( f ). Then there is a randomized [t, Ca, Cb]Bprotocol with error probability 1 3 for solving f. >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> this problem reduces to the predecessor problem >

Highlight ([page.46](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> Corollary 16. In any solution to the prefix parity (and the predecessor) problem, if (n | y| )O(1) cells, each containing logO(1) |U| bits, are used to store the set y, the query time is at least 0(- log log |U| ) as a function of |U| and at least 0(logl 3 | y| ) as a function of | y|. >

### Definitions

Note ([page.38](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

> When the number of rounds of communication is constant, the communication complexity also provides upper bounds for cell probe complexity >  



