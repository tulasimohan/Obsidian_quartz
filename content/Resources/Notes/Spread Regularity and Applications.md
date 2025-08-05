by Shachar Lovett

$\newcommand{\E}{\mathbb{E}}$
$\newcommand{\eps}{\epsilon}$
#### Regularity
- Graph regularity decomposes a graph to parts that "look random".

##### Graph Reguarity
- Szemeredy regularity (1975)
- Freize-Kannan regularity (1996)
- Spread regularity (New)

##### Applications
- Communication
- Matrix multiplication
- Combinatorics

#### Notations
##### Matrices
- Entries: $A(x,y)$
- Size: $|A|$
- Density: $\mathbb{E}[A(x,y)]$
- Rectangle: $R= X \times Y$
- Density in a rectangle: $\mathbb{E}[A|R]$ 

#### Szemeredy Regularity
- Matrix is regular if all its large sub-matrices have same density

>[!def] $\epsilon$-regular
Matrix $A$ is $\eps$-regular if any rectangle $R=X \times Y$ of size
$|R| \geq \epsilon |A|$ satisfies $\mathbb{E}[R]= \E[A] \pm \eps$ 

>[!thm] Theorem [Szemeredi]
>for any $\eps$, any matrix $A$ can be partitioned into $K = K(\eps)$ parts so that most are $\eps$-regular. 

- Szemeredi theorem on 
	- arithmetic progression, 
	- triangle removal lemma, 
	- subgraph counts

- Big caveat: $k(\eps) = 2^{k.^{.^{.}}}$ is a tower of height $poly(1/\eps)$.


#### Frieze-Kannan Regularity
- Let $A$ be a matrix with a partition to rectangles
- Let $B$ be a matrix of the same size, where we can average the values inside each rectangle. 
- The partition is weak-regular if large rectangles cannot differentiate $A,B$. 

>[!def] $\eps-$weak regular
>partition is $\eps$ *weak regular* if any rectangle $R$ of size $|R|\geq \eps |A|$ satisfies 
>$\E[A|R] = \E[B|R] \pm \eps$ 

>[!thm] Frieze-Kannan regularity lemma
>for any $\eps$, any matrix $A$ has a partition into $k = k(\eps)$ parts which is $\eps$-weakly regular.

+ improved number of parts : $k(\eps) = \exp(1/\eps^2)$.
+ weaker guarantees than Szemeredi's regularity lemma. 

#### Spread Regularity

- ***Intuition:*** define "regular" so that violationg it naturally leads to "density increment".

- Improved bounds: $\#$ parts = quasi-polynomial
- weaker guarantess:
	- can no longer argue that a single matrix looks random.
	- however, product of spread-regular matrices is near uniform.

> [!def] Spread regularity
> matrix $A$ is $(d,\eps)$-spread if:
> - $\forall$ rectangles $R$ of size $|R| \geq 2^{-d}|A|$, $\E[A|R] \leq (1+\eps)\E[A]$
> - For any row of $A$, its density is $\geq (1-\eps)\E[A]$ 

fix $\eps = 0.01$, $d\geq 1$ large

- By this def, either the matrix is spread regular or there exists a large sub-rectangle which is spread regular.

##### Mixing

>[!thm] Theorem
>Let $A,B$ be matrices with $\E[A]$, $\E[B] \geq 2^-d$ which are $(poly(d).01)$-spread regular. Then
>$$\Pr_{x,y}\left[0.9 \leq \frac{AB^T(x,y)}{\E[A]\E[B]} \leq 1.1\right] \geq 1- 2^{-d}.$$

$AB^T$ is the normalized matrix product $AB^T(x,y) = \E_z[A(x,z)B(y,z)]$.

>[!cor] Corollary
>if $C$ is a matrix with density $\E[C] \geq 2^-d$ then
$$\E_{x,y,z}[A(x,z)B(y,z)C(x,y)] \sim \E[A]\E[B]\E[C]$$

>[!thm] Theorem
>for any $d$, any matrix $A$ can be partitioned as follows:
>$$A = \sum_{i=1}^k A_i[X_i \times Y_i]$$
>where:
>1. $A_i$  is defined over the rectangle $R_i = X_i \times Y_i$
>2. Either $A_i$ is sparse (\E[A_i] \leq 2^{-d}) of $A_i$ is (d,0.01)-spread regular in $R_i$. 
>3. Few rectangles: $k \leq 2^{poly(d)}$ (quasi-poly in $2^{-d}$). 
>4. Rectangles are an approximate partition: $\sum |R_i| \leq O(d)|A|$.

