$\newcommand{\E}{\mathbb{E}}$

A note based on the paper [[Don't rush into a union - take time to find your roots]]

>[!info] The communication game
>Consider a sequence of $n$ operations $X_1, \dots, X_n$. Each $X_i$ is either an update or a query. We know in advance for each $i$ whether $X_i$ will be an update or a query. However, we do not know the specific update or query content of $X_i$.
>
>Let $I_A$ and $I_B$ be two consecutive intervals of operations within the sequence $X_1, \dots , X_n$. Alice receives 
all operations except those in $I_B$, and Bob receives all operations except those in $I_A$. Their goal is to communicate and determine the answers to the queries in $I_B$​. 
The inputs $X_A$ and $X_B$ of Alice and Bob respectively come from the distribution $D$. 

Define the following the sets of cell of the memory 
$W_A$:= cells written/read during the interval $I_A$.  
$W_B$:= cells  written during the interval $I_B$. 
$R_B$:= cells which are read before they are written during $I_B$. 


>[!tip] Lemma 4 
>For any $p \geq 0$, the communication game can be solved by a zero-error protocol with complexity 
>$$\E_D \left[|W_A| · O\left(\log \frac1p \right) + O(w) · (|R_B \cap (W_A \setminus W_B)| + p|R_B|)\right]$$

***Proof.***

>[!tip] Lemma 5 
>The communication game can be solved by a nondeterministic protocol with complexity 
>$$\E_D \left[O(w) · |W_A \cap R_B| +  O(|W_A \cup R_B|)\right].$$

***Proof.***
**Prover's message** $Z(X_A, X_B)$ of the prover will consist of the 
- addresses and contents of the cells $X = |W_A \cap R_B|$, taking $O(w)$ bits each. 
- In addition, he will provide a retrieval dictionary for the symmetric difference $W_A \Delta R_B = (W_A \setminus R_B) ∪ (R_B \setminus W_A)$. In this dictionary, every element has one associated bit of data: zero if the cell is from $W_A \setminus R_B$ and one if from $R_B \setminus W_A$. The dictionary takes $O(\log w + |W_A \cup R_B|)$ bits.

**Alice** 
- first simulates the data structure on $I_A$. Then she verifies that all cells $X$ were actually written $(X \subseteq W_A)$, and their content is correct. 
- Furthermore, she verifies that for all cells from $W_A \ X$, the retrieval dictionary returns zero. If some of this fails, she rejects with a false.

**Bob** 
simulates the data structure on $I_B$. The algorithm may read cells of the following types: 
• cells previously written during IB: Bob knows their contents. 
• cells from X: Bob uses the contents from public proof (Alice verified these contents). 
• cells for which the retrieval dictionary returns one: Bob uses the contents from the fixed memory snapshot before the beginning of IA (Alice verified she didn’t write such cells). 
• cells for which the retrieval dictionary return zero: Bob rejects. The prover is trying to cheat, since in a correct simulation all cells of $R_B \setminus X$ has a one bit in the dictionary.

If neither player rejects, we know that $R_B \setminus X$ is disjoint from $W_A \setminus X$, so the simulation of Bob is correct. Finally Bob rejects if any of his answers are false.


>[!tip] Theorem 10
 Any data structure for dynamic connectivity in graphs of $n$ vertices that has update time $t_u = o(\log n)$ must have query time t$_q \geq n^{1−o(1)}$.

***Proof.***
- Let $\epsilon$ be such that $t_U = o(\epsilon^2 \log n)$, and define $M = n^{1−\epsilon}$ and  $C = n^\epsilon$.
- The vertices are points of a grid $[M ] \times [n/M ]$. 
- The edges of our graph are matchings between consecutive columns. Let $\pi_1, \cdots , \pi_{n/M−1}$ be the permutations that describe these matchings.
- We let $\pi_{\leq j} = \pi_j ◦ \pi_{j−1} \circ \cdots \circ \pi_1$. Node i in the first column is connected in column $j + 1$ to $\pi_{\leq j}(i)$.>- The graph also contains $C$ special vertices, which we imagine are colored with the colors $1, \dots , C$. At all times, a colored vertex is connected to a fixed set of $M/C$ vertices in the first column.

>[!note] Data structure problem
>- **Update**$(j,\pi_{new})$: sets the permutation between the layers $j$ and $j+1$ to $\pi_{new}$
>- **Query**$(j,\chi)$: given $\chi \in [C]^M$, a coloring of $M$ vertices, checks if this coloring is consistent with the coloring induced in the $j^{th}$ layer by the special vertices . 

^d7f2d7

- each meta-update can be implemented by $2M$ edge updates. Therefore update time = $O(2Mt_U)$ 
- the cell-probe complexity of each meta query is $O(M)\cdot t_U + C\cdot t_q$. 

A QUERY can be implemented efficiently by connectivity operations. 
First each vertex i in column j is connected to the colored vertex χ[i]. 
Then, for $i = 2 \dots M$, we run a connectivity query to test whether colored vertex $i$ is connected to colored vertex $i − 1$. 
If so, QUERY return false. Otherwise, it inserts an edge between colored vertices $i$ and $i − 1$ and moves to the next i. At the end, QUERY deletes all vertices it had inserted. The total cell-probe complexity of QUERY is $O(M) · t_U + C · t_q$.

---

>[!tip] Lemma 11 
>Let $v$ be a node with $2k$ leaves in its subtree, and  let $v_L$, $v_R$ be its left and right children. Then 
>$$\E\left[|W (v_L)\cap R(v_R)|+  \frac1{\log n} |W (v_L) \cup R(v_R)|\right] = \Omega(k · \epsilon M ).$$


>[!tip] Lemma 12 
>The game above has nondeterministic communication complexity $\Omega(kM \log C)$.


**Questions?:**
- What is the abstract property here?
- In the non-deterministic protocol, why is it not enough to run the simulation with just  $O(w \cdot |W_A \cap R_B|)$.



