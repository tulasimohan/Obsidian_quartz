---
{"publish":true,"title":"Time-space trade-offs for predecessor search","created":"2025-05-24T17:36:28.426+01:00","modified":"2025-07-11T13:26:37.592+01:00","published":"2025-07-11T13:26:37.592+01:00","cssclasses":""}
---


# Time-space trade-offs for predecessor search


> [!meta]- Abstract
We develop a new technique for proving cell-probe lower bounds for static data structures. Previous lower bounds used a reduction to communication games, which was known not to be tight by counting arguments. We give the first lower bound for an explicit problem which breaks this communication complexity barrier. 
In addition, our bounds give the first separation between polynomial and near linear space. 
Such a separation is inherently impossible by communication complexity.
Using our lower bound technique and new upper bound constructions, we obtain tight bounds for searching predecessors among a static set of integers. 
Given a set Y of n integers of l bits each, the goal is to efficiently find PREDECESSOR (x) = max (y ∈ Y | y ≤ x). 
For this purpose, we represent Y on a RAM with word length $b$ using $S ≥ nl$ bits of space. Defining $a = \log S/n$, we show that the optimal search time is, up to constant factors: 
$$\min\begin{cases} &\log b n,\\ \\ &\log ( \frac{l-\log n}a)  ,\\ \\ &\frac{\log(l/a)}{\frac{\log a}{\log n} \cdot \log \frac{l}a)},\\ \\  &\frac{\log (\frac{l}a)} {\log (\log (\frac{l}a) / \log (\frac{\log n}a))}\end{cases}$$
>
In external memory $(b > l)$, it follows that the optimal strategy is to use either standard B-trees, or a RAM algorithm ignoring the larger block size. 
In the important case of $b = l = \gamma \log n$, for $\gamma > 1$ (i.e. polynomial universes), and near linear space (such as $S = n \log^{O(1)} n$), the optimal search time is $Θ(\log l)$. 
Thus, our lower bound implies the surprising conclusion that van Emde Boas' classic data structure from [FOCS'75] is optimal in this case. 
Note that for space $n^{1+ε}$, a running time of $O(\log l / \log \log l)$ was given by Beame and Fich [STOC'99].



> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/library/items/L89828GY)
> Authors:: [[people/Mihai Pătraşcu\|Mihai Pătraşcu]], [[people/Mikkel Thorup\|Mikkel Thorup]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/1132516.1132551
> doi:: 
> bibliography:: Pătraşcu, Mihai, and Mikkel Thorup. 2006. ‘Time-Space Trade-Offs for Predecessor Search’. In _Proceedings of the Thirty-Eighth Annual ACM Symposium on Theory of Computing_, 232–40. STOC ’06. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/1132516.1132551](https://doi.org/10.1145/1132516.1132551).


---
## Self Notes


Model:: Static
problems:: [[Problems/Data_Structures/Both/Predecessor\|Predecessor]]
Techniques:: [[probe elimination]] = round elimination + message compression
lbs:: $\min\begin{cases} &\log b n,\\ \\ &\log ( \frac{l-\log n}a)  ,\\ \\ &\frac{\log(l/a)}{\frac{\log a}{\log n} \cdot \log \frac{l}a)},\\ \\  &\frac{\log (\frac{l}a)} {\log (\log (\frac{l}a) / \log (\frac{\log n}a))}\end{cases}$


- [ ] read carefully, this technique is used at other places.  


Q: round elimination + message compression  = probe elimination ?

[[Problems/Data_Structures/Both/Predecessor\|Predecessor]]

$\newcommand{\calD}{\mathcal{D}}$
### Cell probe elimination lemma: 

- Published bits and accepted queries.

#### Direct summing 

>[!def]- $\oplus^kf$
>Given $f: D \times Q \to \{0,1\}$ define its direct-sum version $\oplus^kf : D^k \times ([k] \times Q) \to \{0,1\}$. 
>**Data** : $(d^1, \dots ,d^k) \in D^k$
>**Queries**: $(i,q)$ for $i \in [k]$
 the answer of the query $(i,q)$ on the data point $(d^1, \dots ,d^k)$ is the same as the answer of 
 $q$ on $d^i(q(d^i))$. 
- similarly given a distribution $\calD$, we can define $\oplus^k\calD$.


>[!def]- $f^{(h)}$
>**data:** $d \in \calD$, $r \in [h]$ , $(q_1, \dots, q_{r-1})$
>**queries:** $(q_1,\dots,q_h)$ 
>output of the query: $f(d,q_r)$

**definition:** $\oplus^kf^{(h)} = \oplus^k[f^{(h)}]$

>[!lemma] Lemma 1 
There exist a universal constant $C$, such that for any problem $f$, distribution $\calD$ and positive integers $k,h$ the following holds.
>
>Assume there is a solution to $\oplus^kf^{(h)}$ with accepting probability $\alpha$ over $\oplus^k\calD^{(h)}$, which uses 
>* $k\sigma$ words of space 
>* $\frac1C (\frac{\alpha}{h})^3k$ published bits
>* $T$ cell probes
>
Then there exists a solution to $\oplus^kf$ with accepting probability $\frac{\alpha}{4h}$ over $\oplus^k\calD$ which uses
>- has the same space, 
>- $k \cdot \sigma^{1/h}\cdot Cb^2$ published bits and 
>- $T-1$ cell probes.


>[!DSP] Colored predecessor problem on $n$ integers of $\ell$ bits each
>
>- **$P(n,\ell)$:** predecessor problem on $n$ integers of $\ell$ bits each.
>- A decision version of the Predecessor problem where elements are colored red or blue, and a query just returns the color of the predecessor. 


>[!def] Lemma 2
>
>For any integers $n, \ell ,h \geq 1$, 
and given distribution $\calD$ for $P(n,\ell)$, 
there exists a distribution $\calD^{*(h)}$ for $P(n,h\ell)$ such that the following holds. 
>
Given a solution to $\oplus^kP(n,h\ell)$ with accepting probability $\alpha$ over the distribution $\calD^{*(h)}$,
one can obtain a solution to $\oplus^kP(n,\ell)^h$ with accepting probability $\alpha$ over $\oplus^k\calD^{(h)}$,
which has the same complexity in terms of space, published bits and cell probes.   


>[!lemma] Lemma 3
For any integers $t,\ell, n \ge 1$ and distribution $\calD$  for $P (n,\ell)$, 
>there exists a distribution $\calD^{∗t}$ for $P (n\cdot t, \ell + \log t)$ such that the following holds. 
>- Starting from a solution to  $\oplus^k P(nt, \ell+ \log t)$ with accept probability $\alpha$ over $\oplus^k D^{∗t}$,  
>- one can construct a solution to $\oplus^{kt} P(n,\ell)$ with accept probability $\alpha$ over $\oplus^{kt} D$, which has the same complexity in terms of space, published bits, and cell probes.


>[!lemma] Lemma 4. 
>For any $n \ge 1$ and $\ge \log_2(n + 1)$, there exists a distribution $\calD$ for $P (n,\ell)$ such that the following holds. 
> $\forall 0 < \alpha \le 1$ and $k \ge 1$, there does not  exist a solution to $\oplus^k P (n,\ell)$ with accept probability $\alpha$ over  $\oplus^k \calD$, which uses no cell probes and less than $\alpha k$ published bits.

- base case: no cell probes and only published bits. 





- What is the outline of the proof?   

**Lemma 1:** start with a solution for $\oplus^kf^{(h)}$ and obtain a solution for $\oplus^kf$. 
- This is the probe elimination lemma. 
- Is independent of the function $f$. 

Identify the structure of $P(n,\ell)^{(h)}$ inside $P(n,h\ell)$. 
**Lemma 2:** Given a solution of $\oplus^kP(n,h\ell)$ gets a solution for $\oplus^k P(n,\ell)^{(h)}$.

**Lemma 3**: Given a solution of $\oplus^kP(n t,\ell + \log t)$ gets a solution of $\oplus^{kt}P(n,\ell)$.

**Lemma 4**: No solution with 0 cell probes and bounded published bits.   


## Reading notes



  



