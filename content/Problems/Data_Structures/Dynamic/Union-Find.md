---
{"publish":true,"created":"2025-05-24T17:36:32.326+01:00","modified":"2025-07-09T12:16:40.023+01:00","published":"2025-07-09T12:16:40.023+01:00","cssclasses":""}
---

## Union find

>[!DDSP] Set Union Problem
> This problem concerns the design of a data structure for the on-line manipulation of sets in the following setting. Initially, there are $n$ singleton sets $\{1\}, \{2\},\dots, \{n\}$ with $i$ chosen as the name of the set $\{i\}$. 
>**Query:** 
> *Find($j$):* returns the name of the set containing $j$. 
>**Update:**
> *Union($A$, $B$, $C$)* combines the sets with names $A$ and $B$ and output $C$. 
 

### Boolean Union find

^4f4a4d

In the Boolean union-find problem the find operation is a binary predicate that gets an item $x$and a set $A$ and answers positively if and only if $x \in A$.

**find(x,A)**: is $x \in A$?

### Static Tree Union Find

^32bbc7
