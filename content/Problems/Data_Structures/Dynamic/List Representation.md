

>[!DDSP] List Representation. 
>**Data:** Representation of an ordered list of at most $n$ (not necessarily distinct) elements from the universe $U = \{1, 2,…, n\}$. 
>**Queries:**
>*report(k)*, which returns the $k$th element of the list, 
>**Updates:**
>*delete($k$)*, which deletes the $k$th item.
>*insert(k, u)* which inserts element $u$ into the list between the elements in positions $k - 1$ and $k$, 

## Upper bounds: 

### Vector 
One simple solution to the list representation problem is to maintain a vector $v$, whose $k$th entry contains the $k$th item of the list.
- report = constant time
- insert and delete = linear time 

### Linked list
Alternatively, one could store the items of the list with each element having a pointer to its predecessor and successor in the list. 
- report=  linear time 
- updates = constant time  

### AVL trees 
This problem can be solved must more efficiently by use of balanced trees (such as AVL trees). 
- When $b = \log n$, the worst case cost per operation using AVL trees is $O(\log n)$. 
- If instead $b = 1$, so that each bit access costs 1, then the AVL three solution requires $O(\log^2n)$ per operation.
[[AVL trees]] 

