
>[!DSS] Meldable heap
>The classical meldable heap data type maintains an item disjoint set of heaps subject to the following operations.  
**make-heap:** Return a new, empty heap. 
**insert(i; h):** Insert a new item i with prede ned key into heap h. 
f**ind-min(h):** Return an item of minimum key in heap h. This operation does not change h. 
**delete-min(h):** Delete an item of minimum key from heap h and return it. 
**meld(h1; h2):** Return the heap formed by taking the union of the item-disjoint heaps h1 and h2. This operation destroys h1 and h2. 
**decrease-key( $\Delta$ ; i; h):** Decrease the key of item i in heap h by subtracting the nonnegative real number $\Delta$. 
**delete(i; h):** Delete item i from heap h.

