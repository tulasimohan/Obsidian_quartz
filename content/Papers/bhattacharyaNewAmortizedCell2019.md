---
{"publish":true,"title":"New amortized cell-probe lower bounds for dynamic problems","created":"2025-05-24T17:36:29.724+01:00","modified":"2025-07-07T14:31:55.459+01:00","published":"2025-07-07T14:31:55.459+01:00","cssclasses":""}
---


# New amortized cell-probe lower bounds for dynamic problems


>[!meta]- Abstract
>
>We build upon the recent papers by Weinstein and Yu [11], Larsen [7], and Clifford et al. [3]
to present a general framework that gives amortized lower bounds on the update and query
times of dynamic data structures. Using our framework, we present two concrete results.
>
>1. For the dynamic polynomial evaluation problem, where the polynomial is defined over
a finite field of size n1+ (1) and has degree n, any dynamic data structure must either
have an amortized update time of ((lg n/ lg lg n)2) or an amortized query time of
((lg n/ lg lg n)2).
>
>2. For the dynamic online matrix vector multiplication problem, where we get an
n × n matrix whose entires are drawn from a finite field of size n (1), any dynamic
data structure must either have an amortized update time of ((lg n/ lg lg n)2) or an
amortized query time of (n · (lg n/ lg lg n)2).
>
For these two problems, the previous works by Larsen [7] and Clifford et al. [3] gave the
same lower bounds, but only for worst case update and query times. Our bounds match
the highest unconditional lower bounds known till date for any dynamic problem in the
cell-probe model.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Sayan Bhattacharya\|Sayan Bhattacharya]], [[people/Monika Henzinger\|Monika Henzinger]], [[people/S. Neumann\|S. Neumann]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Bhattacharya, Sayan, Monika Henzinger, and S. Neumann. 2019. ‘New Amortized Cell-Probe Lower Bounds for Dynamic Problems’. [https://doi.org/10.1016/J.TCS.2019.01.043](https://doi.org/10.1016/J.TCS.2019.01.043).

---
## My Notes

Model::Dynamic  
Problems::[[Problems/Data_Structures/Dynamic/Dynamic Polynomial Evaluation\|Dynamic Polynomial Evaluation]], [[Online Matrix Vector Multiplication]] 
Techniques::techniques from [[cliffordNewUnconditionalHardness2015a]] [[WY16]]  [[larsenHigherCellProbe2012a]] 
lbs:: amortized update time of $\Omega((\log n/ \log\log n)^2)$ or amortized query time $\Omega(n \cdot (\log n/ \log\log n)^2)$. 
InorOut:: In 






