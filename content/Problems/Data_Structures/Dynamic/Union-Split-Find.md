
>[!DSP] Union-Split-Find
The Union-Split-Find problem (on intervals)  is the task of implementing a data type  
**Data:** set $S \subseteq [n] = \{1 \dots n\}$, initially empty, 
**Updates**:   
*Union:*  For each $i \in [n]$, the  Union(i) operation removes $i$ from $S$.
*Split:* For each $i \in [n]$, the operation split(i) inserts $i$ into $S$.  
**Queries:** 
*Find:* For each $i \in [n]$, the operation find(i) returns the largest element of $S$ which is smaller  than or equal to $i$ if such an element exists,  otherwise O is returned.


The reason for the names union, split, and find is  the following: 
We can consider the data type as  maintaining the set of intervals  $\{[x; y) | x \in S \cup \{0\}, y \in S \cup \{n+ 1\}, (x;y) \cap S = \emptyset \}$ 
where $[z; y)= \{z, z+1, \dots y-1\}$ and $(z; y) =  \{z+1, z+2,..., y – 1\}$. 

