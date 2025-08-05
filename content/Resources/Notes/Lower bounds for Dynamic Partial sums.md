by [[../people/Mihai Pǎtraşcu\|Mihai Pǎtraşcu]]
$\newcommand{\G}{\mathbb{G}}$
$\newcommand{\bD}{{\bf \Delta}}$
$\newcommand{\abra}[1]{\langle #1 \rangle}$
$\newcommand{\E}{\mathbb{E}}$


>[!note] [[Problems/Data_Structures/Dynamic/Partial Sums\|Partial Sums]]
>Let $\G$ be a group. 
>**Data:** Array $A$ of length $n$ with elements $\in \G$, 
>**Updates**($k$,$\Delta$): $A[k] \leftarrow A[k] + \Delta$ 
>**Queries**($k$): $\sum_{i=1}^k A[k]$

- Upper bound using [[Augmented binary trees]] of $O(\log n)$.
- Let $\delta = \log |G|$, they show a lower bound of $\Omega(\frac{\delta}{w}\log n)$.  

##### The Hard instance
A uniformly random $(\Delta_1, \dots, \Delta_n) \in \G^n$ and $\pi \in \G^n$. 

For $t \leftarrow 1$ to $n$,
	do Query($\pi(t)$),
		Update $(\pi(t),\Delta_t)$.

	
>[!Definition] Information Transfer
>$IT(t_0,t_1,t_2)$ is the collection of cells which were
>- read at time $t_r \in [t_1,t_2]$
>- written during $t_w \in [t_0,t_1]$ and not in $[t_w+1,t_2]$. 

Let $\bD = \abra{\bD_1, \dots ,\bD_n}$ be the random updates and $\bD_{[t_0,t_1]}$ denote the the updates in the interval $[t_0,t_1]$ and $\Delta^*$ denote the rest of the updates. 
Let $\alpha_{[t_1,t_2]} :=\abra{\alpha_{t_1},\dots, \alpha_{t_2}}$ be the answers to the queries in the second interval.

>[!Lemma] Lemma 2
>$$H(\alpha_{[t_1,t_2]}|\Delta^* = \bD^*) \leq w + 2w \cdot \E [IT(t_0,t_1,t_2)|\Delta^*=\bD^*]$$

>[!Def] Interleave number
>$IL(t_0,t_1,t_2)$
