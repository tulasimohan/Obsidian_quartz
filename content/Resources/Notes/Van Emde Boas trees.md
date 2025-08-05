Peter Van EmdeBoas

Problem:: Predecessor Problem
**Model**: integers from a universe $U$. 
**Task**: Maintain $n$ elements from a universe $U$. 
**operations**: insert, delete, successor 

- Binary Search Trees $O(\log n)$. 
- Van Emde Boas $O(\log \log U)$. 

Application : Network routers

###### Where does $\log \log U$ come from?

- Binary search on the levels of the trees. 
- Recurrence: 
	- $T(U) = T(\sqrt{U}) + c$

###### Attempt 1: 
- $O(1)$ Insert and Delete. Forgetting Successor. 

- Ans: Bit vector O(U)

###### Attempt 2:

- Bit vector size $U$. 
- Split the Universe into galaxies/ clusters. 
	- store the OR of the bits within each cluster. Call this the summary vector.  $O(\sqrt{U})$

###### Attempt 3:
- Recurse	$O(\log n)$ or $O(\log n)^{\log_2 3}$

###### Attempt 4: 
- store the min and max.  
- $O(\log \log U)$ for successor
- need to fix the update time 