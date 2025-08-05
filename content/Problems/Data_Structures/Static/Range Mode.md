Mode of a multi-set is the most frequent element ins the 

>[!DSP] Range Mode
**Data:** The input to the range mode problem is an array A of size n. 
**Queries:** A range query [i, j] must return the mode of the subarray A[i], A[i + 1], . . . , A[j]

### Upper bounds 

Constant query upper bounds. 

| Authors                             | space upper bound              | year |
| ----------------------------------- | ------------------------------ | ---- |
| Krizanc, D., Morin, P., Smid, M.H.M | $O(n^2 \log \log n/\log n)$    | 2005 |
| Petersen, H.                        | $O(n^2/\log n)$                | 2008 |
| Petersen, H., Grabowski, S          | $O(n^2 \log \log n/ \log^2 n)$ | 2008 |

Non-constant query upper bounds

| Authors                             | space upper bound | query upper bound      | year |
| ----------------------------------- | ----------------- | ---------------------- | ---- |
| Krizanc, D., Morin, P., Smid, M.H.M | $O(n^{2−2ε})$     | $O(n^\epsilon \log n)$ | 2005 |
| Petersen, H.                        | $O(n^{2−2ε})$     | $O(n^\epsilon)$        | 2008 |





## Approximate range mode 

>[!DSP] c-approximate range mode
>return any label that occurs atleast $1/c$ fraction of mode. 


| Authors                                     | approximation factor | space                   | Query time                                 |
| ------------------------------------------- | -------------------- | ----------------------- | ------------------------------------------ |
| Bose, P., Kranakis, E., Morin, P., Tang, Y. | 2                    | $O(n \log n)$           | $O(1)$                                     |
|                                             | 3                    | $O(n \log \log n)$      | $O(1)$                                     |
|                                             | 4                    | $O(n)$                  | $O(1)$                                     |
|                                             | $1+\epsilon$         | $O(\frac{n}{\epsilon})$ | $O(\log \log n \cdot \log \frac1\epsilon)$ |
