---
{"publish":true,"title":"Weistein@Super- logarithmic DSLB","created":"2025-05-24T17:36:35.630+01:00","modified":"2025-05-24T17:36:31.151+01:00","published":"2025-05-24T17:36:31.151+01:00","cssclasses":""}
---

#talk

##### Outline 
- Intro
- Static Data structures 
	- Eg: Reachability
- Dynamic model
	- Eg: Employee salary 
- Cell probe model 
	- (w,n)
		- word size = w
		- no. of update/ queries = n
	- non-uniform model of computation
- Queries and updates

| Authors           | Bound                               | Problem                 | Year |
| :---------------- | ----------------------------------- | ----------------------- | ---- |
| Fredman, Saks     | $\Omega(\frac{\log n}{\log log n})$ | Prefix-sum              | 1989 |
| Patrascu, Demaine | $\Omega(\log n)$                    | Connecticity            | 2004 |
| Larsen            | $\Omega(\log^2 n)$                  | Weighted range counting | 2012 |
|                   |                                     |                         |      |
- Pat'07, PT'08, CGL'15,WY'16, ... all of them are for non-boolean query output. 


- Super logarithmic lower bounds

> [!NOTE] ***This Work***:
> An $\Omega(\log^{1.5} n)$ LB for many version of classical DS problems. 
> - A range counting over $\mathbb{F}_2$.
> - $\omega(\log n)$ LB for classical 2D rage counting (UB:$O(\log^2 n)$).

- Kasper's lb High-level idea
	n points in the 2D grid 
	- let $\beta = t_u \cdot  w$ and divide the updates into epochs of size $\beta^i$ for $i \in [\log_\beta n]$.
	- suppose there is an epoch with $t_q/\log_\beta n$ queries in expectation, then we can get a too-good to be true protocol.   
 	Pre-initialization + Static problem + Cache


- Decoding
- Approach

Mihai solved it with a Bloom filter in Patrascu-Demaine. 

Code: 

Update sequence to a code ->  Query vector
$(U_1, \dots, U_r) \to \{0,1\}^{|Q|}$ 

- list decoding radius of a random code is $1/2$. 
- list decoding = higher moments

##### Peak to average lemma
Let r.v. $Z = Z_1, \dots, Z_k$, $B$(uniform) binary r.v. in same prob space such that 

>[!Note] ***Peak to Average***
 Let $f:\{0,1\}^k \to \mathbb{R}$ s.t. (i) $|f|_1 \leq 1$  and (ii) $|f|_\infty \geq \epsilon$ 
> $$\implies \exists |Y| \leq O(\sqrt{k\cdot \log 1/\epsilon}) \ s.t.\  |\sum_{z|Y =1} f(z)| \geq exp(-\sqrt{k\cdot \log 1/\epsilon}).$$


- The property that is actually required in Larsen Yu is k-wise independence. 
#### Thoughts 
- Do static lower bounds dynamic lower bounds?
- Do dynamic lower bounds imply static lower bounds? 
- What is the property ? 
