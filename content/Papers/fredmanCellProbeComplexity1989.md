---
{"publish":true,"title":"The cell probe complexity of dynamic data structures","created":"2025-05-24T17:36:28.076+01:00","modified":"2025-07-11T13:17:04.329+01:00","published":"2025-07-11T13:17:04.329+01:00","cssclasses":""}
---


# The cell probe complexity of dynamic data structures


>[!meta]- Abstract
Dynamic data structure problems involve the representation of data in memory in such a way as to permit certain types of modifications of the data (updates) and certain types of questions about the data (queries). This paradigm encompasses many fundamental problems in computer science.The purpose of this paper is to prove new lower and upper bounds on the time per operation to implement solutions to some familiar dynamic data structure problems including 
list representation, subset ranking, partial sums, and the set union problem.
 
The main features of our lower bounds are:
- They hold in the cell probe model of computation (A. Yao [18]) in which the time complexity of a sequential computation is defined to be the number of words of memory that are accessed. (The number of bits $b$ in a single word of memory is a parameter of the model). All other computations are free. This model is at least as powerful as a random access machine and allows for unusual representation of data, indirect addressing etc. This contrasts with most previous lower bounds which are proved in models (e.g., algebraic, comparison, pointer manipulation) which require restrictions on the way data is represented and manipulated.
- The lower bound method presented here can be used to derive amortized complexities, worst case per operation complexities, and randomized complexities.
- The results occasionally provide (nearly tight) tradeoffs between the number $R$ of words of memory that are read per operation, the number $W$ of memory words rewritten per operation and the size $b$ of each word. 
- For the problems considered here there is a parameter $n$ that represents the size of the data set being manipulated and for these problems $b = \log n$ is a natural register size to consider. By letting $b$ vary, our results illustrate the effect of register size on time complexity. For instance, one consequence of the results is that for some of the problems considered here, increasing the register size from $\log n$ to $poly-log(n)$ only reduces the time complexity by a constant factor. On the other hand, decreasing the register size from $\log n$ to 1 increases time complexity by a $\log n$ factor for one of the problems we consider and only a $\log\log n$ factor for some other problems.The first two specific data structure problems for which we obtain bounds are:

>[!DDSP] List Representation. 
>**Data:** Representation of an ordered list of at most $n$ (not necessarily distinct) elements from the universe $U = \{1, 2,…, n\}$. 
>**Queries:**
>*report(k)*, which returns the $k$th element of the list, 
>**Updates:**
>*delete($k$)*, which deletes the $k$th item.
>*insert(k, u)* which inserts element $u$ into the list between the elements in positions $k - 1$ and $k$, 


>[!DDSP] Subset Rank. 
>**Data:** representation of a subset $S$ of $U = \{1, 2,…, n\}$. 
>The operations that must be supported are the 
>**updates**
>*insert:* “insert item j into the set” and 
>*delete:* “delete item j from the set” and 
>**queries:** 
>*rank(j)*, which returns the number of elements in $S$ that are less than or equal to $j$.


>The natural word size for these problems is $b = \log n$, which allows an item of $U$ or an index into the list to be stored in one register.

It is not hard to find similar upper bounds for the subset rank problem (the algorithms for this problem are actually simpler than AVL trees).
The question is: are these upper bounds bet possible? Our results show that the upper bounds for the case of $\log n$ bit registers are within a $\log\log n$ factor of optimal. 
On the other hand, somewhat surprisingly, for the case of single bit registers there are implementations for both of these problems that run in time significantly faster than $O(\log^2n)$ per operation.

Let CPROBE(b) denote the cell probe computational model with register size b.
- Theorem 1. If $b ≤ (\log n)t$ for some $t$, then any CPROBE(b) implementation of either list representation or the subset rank requires $Ω(\log n/\log\log n)$ amortized time per operation.
- Theorem 2. Subset rank and list representation have CPROBE(1) implementations with respective complexities $O((\log n)(\log\log n))$ and $O((\log n)(\log\log n)^2)$ per operation.
- Paul Dietz (personal communication) has found an implementation of list representation with $\log n$ bit registers that requires only $O(\log n/\log\log n)$ time per operation, and thus the result of theorem 1 is best possible.
The lower bounds of theorem 1 are derived from lower bounds for a third problem:

>[!DSP] Partial Sum mod $k$. 
>**Data:** An array A[1],…, A[N] of integers mod $k$ is to be represented. 
>**Updates:** are 
>*add(i, δ):* which implements $A[i] ← A[i] + δ$; and 
>**Queries:** are 
>*sum(j):* which returns $\sum_{i≤j}A[i] (\mod k)$.

This problem is demoted PS(n, k). 


Our main lower bound theorems provide tradeoffs between the number of register rewrites and register reads as a function of $n$, $k$, and $b$. 
Two corollaries of these results are:
- Theorem 3. Any CPROBE(b) implementation of $PS(n, 2)$ (partial sums mod 2) requires $\Omega(\log n/(\log\log n + \log b))$ amortized time per operation, and for $b ≥ \log n$, there is an implementation that achieves this. In particular, if $b = Θ((\log n)^c)$ for some constant $c$, then the optimal time complexity of PS(n, 2) is $\Theta(\log n/\log\log n)$.
- Theorem 4. Any CPROBE(1) implementation of $PS(n, n)$ with single bit registers requires $\Omega((\log n/\log\log n)^2)$ amortized time per operation, and there is an implementation that achieves $O(\log^2n)$ time per operation.
- It can be shown that a lower bound of $PS(n, 2)$ is also a lower bound for both list representation and subset rank (the details, which are not difficult, are omitted from this report), and thus theorem 1 follows from theorem 3. The results of theorem 4 make an interesting contrast with those of theorem 2. For the three problems, list representation, subset rank and PS(n, k), there are standard algorithms that can be implemented on a CPROBE($\log n$) that use time $O(\log n)$ per operation, and their implementations on CPROBE(1) require $O(\log^2n)$ time. Theorem 4 says that for the problem PS(n, n) this algorithm is essentially best possible, while theorem 2 says that for list representation and rank, the algorithm can be significantly improved. In fact, the rank problem an be viewed as a special case of PS(n, n) where the variables take on values on {0, 1}, and apparently this specialization is enough to reduce the complexity on a CPROBE(1) by a factor of $\log n/\log\log n$, even though on a CPROBE($\log n$) the complexities of the two problems differ by no more than a $\log\log n$ factor.

The third problem we consider is the set union problem.
>[!DDSP] Set Union Problem
> This problem concerns the design of a data structure for the on-line manipulation of sets in the following setting. Initially, there are $n$ singleton sets $\{1\}, \{2\},\dots, \{n\}$ with $i$ chosen as the name of the set $\{i\}$. 
>**Query:** 
> *Find($j$):* returns the name of the set containing $j$. 
>**Update:**
> *Union($A$, $B$, $C$)* combines the sets with names $A$ and $B$. 
 

 The names of the existing sets at any moment must be unique and chosen to be integers in the range from 1 to 2n. The sets existing at any time are disjoint and define a partition of the elements into equivalence classes.A well known data structure for the set union problem represents the sets as trees and stores the name of a set in the root of its corresponding tree. A Union operation is performed by attaching the root of the smaller set as a child of the root of the larger set (weight rule). A Find operation is implemented by following the path from the appropriate node to the root of the tree containing it, and then redirecting to the root the parent pointers of the nodes encountered along this path (path compression). From now on we consider sequences of Union and Find operations consisting of n-1 Union operations and m Find operations with m ≥ n. Tarjan [14] demonstrated that the above algorithm requires time θ(mα(m, n)), where α(m, n) is an inverse to Ackermann's function, to execute n-1 Union and m Find operations. In particular, if m = θ(n), then the running time is almost, but not quite, linear. Tarjan conjectured [14] that no linear time algorithm exists for the set union problem, and provided significant evidence in favor of this conjecture (which we discuss in the following section). We affirm Tarjan's conjecture in the CPROBE(logn) model.Theorem 5. Any CPROBE(logn) implementation of the set union problem requires Ω(mα(m, n)) time to execute m Find's and n-1 Union's, beginning with n singleton sets.N. Blum [2] has given a logn/loglogn algorithm (worst case time per operation) for the set union problem. This algorithm is also optimal in the CPROBE(polylogn) model.The following Section provides further discussion of these results, Section 3 outlines our lower bound method, and Section 4 contains some proofs.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/4XQ7ZPYT)
> Authors:: [[people/M. Fredman\|M. Fredman]], [[people/M. Saks\|M. Saks]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/73007.73040
> doi:: 
> bibliography:: Fredman, M., and M. Saks. 1989. ‘The Cell Probe Complexity of Dynamic Data Structures’. In _Proceedings of the Twenty-First Annual ACM Symposium on Theory of Computing_, 345–54. STOC ’89. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/73007.73040](https://doi.org/10.1145/73007.73040).


---
## Self Notes

Techniques::[[Techniques/Dynamic/Chronogram\|Chronogram]]
problems:: [[Problems/Data_Structures/Dynamic/Partial Sums\|Partial Sums]], [[Problems/Data_Structures/Dynamic/List Representation\|List Representation]], [[Problems/Data_Structures/Dynamic/Subset Rank\|Subset Rank]], [[Problems/Data_Structures/Dynamic/Union-Find\|Set Union]]
lbs:: Partial Sums:$\Omega(\frac{\log n}{\log log n})$,
Model:: Dynamic 





## Reading notes



  



