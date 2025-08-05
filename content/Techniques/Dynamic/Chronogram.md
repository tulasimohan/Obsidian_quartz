>[!Note] **Prefix-sum**
>**Data:** Array of length $n$, with entries from $[2^b]$.  
>**Updates:** $\forall i \in [n], x \in [2^b]$, update $(i,x)$ replaces the $i^{th}$ location in the array with $x$.  
>**Queries:** $\forall i \in [n]$ returns the sum of the first $i$ elements in the array. 

Suppose there is a data structure for the Prefix-sum problem with update time $t_u$ and query time $t_q$. Let $\beta = t_u w$ where $w$ is the cell size. 

We perform a sequence of random updates $\bf{U}$, followed by a random query $\bf{j}$.       
- The updates are divided into $\log_\beta n$ epochs $\bf{U}= \bf{U}_{\log_\beta n} \cdots \bf{U}_1$, where in the $i^{th}$ epoch $\bf{U}_i$, we perform $\beta^i$ updates on the set of locations $L_i = \{\frac{j \cdot n}{\beta^i}: j \in [\beta^i]\}$ ^[$\frac{j\cdot n}{\beta^i}$ is assumed to be an integer.] 
Each update replaces a given location of the Array with a random value $x$. The updates from epoch $\log_\beta n$ happen first and epoch 1 happens at the end. 
- Let $\bf{C}_i(\bf{U})$ denote the set of cells in the memory which are last updated during the $i^{th}$ epoch. 


> [!info] ***Claim***
>For $j \in [n]$, let $\bf{Q_j}$ denote the random set of locations probed on the $j^{th}$ query. For all $i \in [\log_\beta n]$, 
>$$\mathbb{E}_{\bf{U},\bf{j}}[|\bf{C_i}(\bf{U}) \cap \bf{Q}_j(\bf{U})|] = \Omega(1)$$     

Given the claim, let us see how to finish the proof.
The expected number of queries made a random query, after applying a random sequence of updates is given by $\sum_{i=1}^{\log_\beta n} \mathbb{E}_{\bf{U},\bf{j}}[|\bf{C_i}(\bf{U}) \cap \bf{Q}_j(\bf{U})|] = \Omega(\log_\beta n )$. 

Now all that is left is to see the proof of the claim.  Note that till now we haven't used any property of the problem other than its skeleton. 

Suppose there is an epoch $i \in [\log_\beta n]$ such that $\mathbb{E}_{U,i}[|C_i(U) \cap Q_j(U)|] = o(1)$. We arrive at a contradiction using the following two player communication game. 

Alice gets $U_1, \ldots, U_{\log_\beta n}$. 
Bob gets $U_1,\dots, U_{i-1},U_{i+1},\dots, U_{\log_\beta n}$ and the query $j$. 
Their goal is to discover the updates $U_i$.

###### The protocol
- Bob simulates the updates till epoch $i$ and arrives at a memory state by the time of epoch. 
- Alice sends $O(\sum_k^{i-1} \beta^{k}t_u)$ bits which correspond to the contents of the cells in which are updated after epoch $i$. With this information, Bob can correctly simulate the updates which do not touch $C_i$.  
- Alice and Bob simulate all the queries with the existing memory state. Since, very few queries touch $C_i$, so $(1 - \epsilon)$ fraction of the updates can be recovered without $C_i$.

##### Decodinq the updates from the corrupted queries: 
- Since the updates in the $i^{th}$ epoch occur in the set of locations $L_i = \{\frac{j \cdot n}{\beta^i}: j \in [\beta^i]\}$. Let $I_{i,j} =  [\frac{j\cdot n}{\beta^i}, \frac{(j+1)\cdot n}{\beta^i}]$ denote the interval between two successive update locations. 

## Chronogram is Natural
$\newcommand{\calH}{\mathcal{H}}$

>[!def] The table
>**Data**: $x \in \{0,1\}^n$   
>**Queries**: $i \in [n]$.  
>**function**: $\sum_{j \leq i} x_j$ 


**Property:** 

Define a Chain of sub-cubes. 

for each sub-cube, 
the columns looks like code words, i.e. they can be decoded by probing a constant fraction of the locations. 

---

Let $\calH$ be a group.
Prefix-Sum over a group $\calH$:   
$D = \calH^n$,
$Q = [n]$
$A = \calH$
G = Hamming graph on $\calH^n$. 
$f(x,i) = \sum_{j=1}^i x[j]$  
Look at standard defs of Prefix sum. 

Suppose $(D,Q,A,f,G)$ be a Dynamic Data Structure Problem with the same skeleton as Prefix Sum. 

**The Property:**
	The rows of the table form an error correcting code. 

## References

