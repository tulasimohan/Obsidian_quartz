$$\newcommand{\cQ}{\mathcal{Q}} \newcommand{\cD}{\mathcal{D}}\newcommand{\poly}{\mathrm{poly}} \newcommand{\ZO}{\{0,1\}}\newcommand{\eps}{\epsilon} \newcommand{\E}{\mathbb{E}} \newcommand{\cA}{\mathcal A} \newcommand{\c}[1]{\mathcal{#1}}$$
## Chronogram + Cell Sampling 

Building on the Chronogram technique for proving Dynamic data structures, Larsen proved a $\tilde\Omega(\log^2 n)$ lower-bound for 2D Range Counting [CITE Larsen 12A] and Polynomial evaluation [Larsen 12B]. 

This is by far the highest known lower bound for Dynamic Data strucrues. However there is one caveat that the set of possible answers $\mathcal{A}$ is not boolean, but $|\mathcal{A}| = n^{\Omega(1)}$. In an earlier work Patrascu showed a $\tilde\Omega(\log^2 n)$ lower bound but for a problem where the set of possible answers $\mathcal{A}$ is super-polynomial in $\log n$. 

- [ ] what is $n$?


Recall that in the Chronogram technique proceeds as follows. 

Here we are going to present a proof using this technique for the Dynamic Polynomial Evaluation problem where the domain $\cD = \F_p^n$ is the set of representations of polynomials of degree exactly $n$ using their roots. \footnote{A polynomial can have multiple representations.} For example, the polynomial  $(x- \alpha_1) \dots (x -\alpha_n)$ is represented by $(\alpha_1, \dots , \alpha_n)$. 

The set of queries $\cQ$ we are going to assume is an arbitrary subset of $\F_p$ of size $p^{1/4}$ where $p = n^{2}$\footnote{any $p = n^{1 + \Omega(1)}$ works}.  
The update graph in the Domain $\cD = \F_p^n$ is that of the Hamming cube., the set of answers $\cA = \F_p$.  The function $f$ is given by polynomial evaluation. 

Suppose there is a $(s,w, t_q,t_u)$ solution for a $(\cD, \cQ,\cU,\cA,f)$ data structure problem where $|\cD| = p^n$,  $|\cQ| = m$ ,  $s = n^{O(1)}$, $m = p^{1/4}$ and $w = O(\log n)$.
- [ ] Be careful with what $s$ is $n^{O(1)}$ is too generous and wrong as there is an upper bound using $p\log p$ space and $O(1)$ reads in the static setting. 

Recall that in the Chronogram technique, we start with the encoding $E(x)$ of an arbitrary element $x \in \F_p^n$ and perform a bunch of updates which are divided into epochs of geometrically decreasing sizes. 
Let $\beta = \log (t_uw)$ and $\bar{U} = U_1,\dots, U_k$ where the $i$th epoch makes $\frac{n}{\beta^i}$ updates. Similar to the Chronogram technique, we assign a color from $[k]$ to each memory location based on the epoch they are last updated. Let $S_1, \dots ,S_k$ be random variables which are the color classes according to this coloring. Let $P(q)$ be the random variable which is the set of locations probed by the random query. The original technique claimed that for $1- o(1)$ fraction of the updates, a random query needs to make at least $O(1)$ reads from each color class. i.e. for all $i \in [k]$,  $\E_{U,q}[|P(q) \cap S_i|] = \Omega(1)$. 

Larsen strengthened this claim to show that the number of reads per from each color class need to be $\Omega(\log n)$.  That is for all epochs $i \in [k]$,  

$$
\E_{U,q}[|P(q) \cap S_i|] = \Omega(\log n) 
$$

- [ ] need to be precise with these numbers.  
Since the number of epochs  is $\log_\beta n$ , this gives a $\tilde\Omega(\log^2 n)$ lower bound. 
We prove this claim by assuming the negation of $\ref{eq: reads_per_epoch}$ and  arriving at a contradiction by showing an compression of $\F_p^n$ to $o(n \log p)$ bits. 
The claim is proved using ideas from cell sampling. 



Suppose there exits an epoch  $i \in [k]$ such that $\E_{U,q}[|S_i \cap S(q)|] = o(\log n)$.

Suppose there is an epoch $i \in [k]$ such that,  $\E_{U,q}[|S_i \cap S(q)|] = o(\log n)$. By an averaging argument, there is a setting of the updates from all the other epochs $U_1, \dots , U_{i-1},  U_{i+1}, \dots , U_{k}$ such that $\E_{U_i,q}[|S_i \cap S(q)|] = o(\log n)$. 

By a Markov style argument, we get that $\Pr_{U_i}[\E_{q}[|S_i \cap S(q)| = o(\log n)]] = \Omega(1)$. 
- [ ] be a bit more precise with the numbers.  

In the original chronogram technique, we argued that a $1-o(1)$ fraction of the queries can be answered without reading any cell from $S_i$. 
In contrast, we now are going to argue that a $n^{-O(1)}$ fraction of the queries can be answered by probing only a $o(\log n)$ reads from $S_i$. 

That is for most(1-o(1)) of the updates, there are a constant fraction of the queries make $o(\log n)$ reads from the $i$th epoch. 
Now we can do cell sub-sampling and and answer a sub-collection of these queries.
In total we will be able to answer an inverse polynomial  fraction of the queries by sampling --- cells. 




---

-> How to shave the $\log \log (t_u w)$ in the denominator? 
**Question**: Can Information transfer technique be used to shave off the $\log$ factors in the denominator?


- [ ] possibly even cell sampling can be improved by using some Erdos-Ko-Rado lemmas or some robust versions of them. 
- [ ] Cell sampling suggests that there is a small set of coordinates which answers a lot of queries. How about making this also adaptive, i.e picking another set of locations based on the contents of these cells. 

How to use Chronogram to prove lower-bound for Polynomial Evaluation? 

Bunch of Queries and Updates, 

Construct a time tree whose leaves are labelled from left to right with  1 to $2^h$, 
For each leaf node in the time tree, make a query and a update. 

For each internal node in the time tree, 

---

