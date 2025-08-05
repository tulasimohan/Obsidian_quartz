
>[!DSP] ball-inheritance problem 
**Data:** the input is a complete binary tree with $n$ leaves. 
>- In the root node, there is an ordered list of n balls. Each ball is associated with a unique leaf of the tree and we say the ball reaches that leaf. 
>- Every internal node v also has an associated list of balls, containing those balls reaching a leaf in the subtree rooted at v. 
>- The ordering of the balls in v’s list is the same as their ordering in the root’s list. We think of each ball in v’s list as being inherited from v’s parent. 
>
>**Queries:** A query is specified by a pair $(v, i)$ where $v$ is a node in the tree and $i$ is an index into $v$’s list of balls. The goal is to return the index of the leaf reached by the $i$’th ball in $v$’s list of balls.


