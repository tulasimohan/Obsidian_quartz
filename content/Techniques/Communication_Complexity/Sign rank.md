>[!def] Sign rank
>The **sign rank** of a real matrix $M$ with no zero entries is the *minimum rank* of a matrix $A$ such that:
$sign(A_{i,j})=sign(M_{i,j}) \forall i,j$

Lower bounds: 
- High sign rank $\implies$ function cannot be computed by PP, UPP,  BQP

>[!thm] Foster's theorem '2002
>$rank_{\pm}(M)$ $\geq \frac{\sqrt{|X||Y|}}{||M||}$ where $||M||$ is the spectral norm of $M$. 

- random functions have sign rank $\Omega(2^{n/2})$. 


# Approximate log-rank and gamma2 norm
$\newcommand{\calX}{\mathcal{X}}$
$\newcommand{\calY}{\mathcal{Y}}$
$\newcommand{\rank}{\mathrm{rank}}$

$F:\calX \times \calY \to \{0,1\}$ or $\{-1,1\}$


#### Rank 
- $\rank(M_F) \leq 2^{D^{CC}(F)}$ or  $\log \rank(M_F) \leq D^{CC}(F)$ 

- **rank** in the communication world is analogous to the **sparsity** in the Query world
- where rectangles are analogous monomials.  
  
How far can we take this analogy?   

- Which tricks that can be performed over polynomials can also be performed over Matrices?

#### Approximate rank

- $\widetilde{\rank}(F) = \min \{\rank(M): |M - M_F|_\infty \leq \epsilon\}$ 

**Question**: How hard is it compute the approximate rank? 

- $\log \widetilde{\rank}(F) \leq Q^{CC}_\epsilon$ in the non-shared entanglement model. 

#### $\gamma_2$ norm
- $Q_\epsilon^{CC} \geq \log \widetilde{\gamma_2}(F)$ with shared entanglement. 

$\log$ of approximate $\gamma_2$ norm and $\log$ of approximate $\rank$ are related. (close) 

#### Approximate $\gamma_2$ norm

- $\tilde{\gamma}_2^\epsilon(F) = \min_{A \approx_\epsilon M_F} \gamma_2(A)$

- $|A|_\infty \leq \gamma_2(A) \leq |A|_\infty \sqrt{\rank(A)}$

 >[!obs] $\gamma_2$ is a norm
 >
 >- $\gamma_2(\lambda A) = |\lambda|\gamma_2(A)$
 >- $\gamma_2(A) = 0 \implies A = 0$
 >- $\gamma_2(A + B) \leq \gamma_2(A) + \gamma(B)$

#### Properties of $\gamma_2$ norm
- $\gamma_2(A \otimes B) = \gamma_2(A) \gamma_2(B)$
- $\gamma_2(A \circ B) \leq \gamma_2(A)\gamma_2(B)$ where $\circ$ is the hadamard product
- if $C$ is a sub-matrix of $A$, $\gamma_2(C) \leq \gamma_2(A)$
- rearranging the rows does not change $\gamma_2$. 

>[!def] $\gamma_2$ norm
 $$\gamma_2(A) := \min_{B,C: BC = A} |B|_r |C|_c$$ 
>where $|B|_r$ is the maximum 2-norm of a row of $B$, and $|C|_c$ is the maximum $2$ norm of a column of $C$. 

>[!def] Equivalent definition of $\gamma_2$ norm
$$\gamma_2{A} = \max_{B \neq 0} \frac{|A \circ B|}{|B|}$$ where $||$ is the spectral norm. 

? filtered $\gamma_2$ norm | negative adversary bound

>[!def] Grothendieck's inequality
>$\gamma_2(A) \approx \nu(A)$

>[!def] Nuclear norm: 
$\nu(A)$ is given by decomposition of  $A$ into a linear combination of $\rank$ 1 sign matrices.

$\min \sum_R |C_R|$ s.t. $\sum_R C_R \cdot R = A$. 

>[!thm] Sherstov '05 lifting theorem
$f:\{0,1\}^n \to \{0,1\}$ and $IP_2: \{0,1\}^2 \times \{0,1\}^2 \to \{0,1\}$

$\widetilde{\rank_\epsilon}(f \circ G) \geq \tilde\Omega(\widetilde\deg_\epsilon(f))$


- The Pattern matrix method