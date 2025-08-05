- [[Problems/Data_Structures/Both/Range_Queries/Range Median]] is a special case

>[!DSP] Range selection  
>**Data:** Preprocess an input array $A$ of $n$ unique integers, such that 
>**Query:** given a query $(i, j, k)$, one can report the $k^{th}$ smallest integer in the subarray $A[i], A[i + 1], …, A[j]$.

### Range Median
choosing $k = \lfloor(i-j)/2\rfloor$, Range Median is an instance of Range selection.   
### Prefix selection 
*prefix selection*, arises when $i$ is fixed to 0 in the Range selection problem.  


### Bounded rank prefix selection 
- Finally, we also consider the *bounded rank prefix selection* problem and the *fixed rank range selection* problem. In the former, data structures must support prefix selection queries under the assumption that $k ≤ κ$ for some value $κ ≤ n$ given at construction time, while in the latter, data structures must support range selection queries where $k$ is fixed beforehand for all queries. 


### Fixed rank range selection

problems:: [[../../Problems/Data_Structures/Static/Range selection\|Range selection]], Prefix selection, Bounded rank prefix selection, Fixed rank range selection