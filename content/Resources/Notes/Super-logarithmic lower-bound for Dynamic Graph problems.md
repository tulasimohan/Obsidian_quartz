$\newcommand{\F}{\mathbb{F}}$
$\newcommand{\calB}{\mathcal{B}}$

>[!Def] Butterfly graph $\calB_{d,B}$
> ***vertices:*** $V_{d,B} = [d+1] \times [B^d]$
> ***edges:***  $\forall i \in [d]$ $\exists$ an edge between $(i,u)$ and $(i+i,v)$ iff $\Delta_H(u,v) \leq 1$. $E_{d,B}$ is the set of edges. 

- $\forall u,v \in[B^d]$, there is a unique path between $(1,u)$ and $(d+1,v)$ in $\calB_{d,B}$. Let $path_{d,B}(u,v)$ denote this unique path. 


>[!problem] 0- xor in Multiple Butterflies 
> ***Data***: $\prod_{i=1}^d E_{i,B} \to \F_2^b$ 
> ***Updates***: for each edge $e \in \cup_{i=1}^d E_{i,d}$, the update $U_e$ assigns updates the label of the edge $e$ with an element of $\F_2^b$.
> ***Queries***:  $q_{u,v}$ $\forall u,v \in [B^d]$.

- Chronogram

- Dynamic to Static

- Tensoring to remove bias  

- Discrepancy bound 
	
- Weak Simulation 
	- Peak to Average
