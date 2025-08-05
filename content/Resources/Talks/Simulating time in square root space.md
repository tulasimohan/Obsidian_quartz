
**Question**: How space efficient can time bounded computation be?


>[!Problem] Circuit Value Problem (CVP)
>**Input**: circuit $C$ of size $s$ and input $x$. 
>Ouput: $C(x)$   

1970: [HPV'77] Hopcroft, Paul, Valiant 
1976: [PV'76] Patterson, Valiant CVP in $O(\frac{s}{\log s})$. 

- these results use a Pebbling approach.  
- Lower bounds: Pebbling approache has a limit of $\Omega(s/\log s )$. 

Model: Multitape Turing Machine (MTM)

- constant($k$) number of tapes.
- Input is in tape 1. Rest of the tapes are blank initially. 
- Each tape head moves independently according to the transition function. 
- read, write cells. 

>**Open problem:** 
> Find a problem which is solvable in linear time by a random acces machine and cannot be solved by a multi tape(constant) machine. 

Upto poly-log factors in the running time, 
- CVP 
- Sorting 
- FFT
- Matrix-Mul
can be done on multi-tape TM with a poly-log overhead compared to the RAM model.

>[!Theorem] 
$TIME (t) \subseteq SPACE(\sqrt{t \log t})$

> [!Cor] Corollary
> - $CVP \in SPACE(\sqrt{n} \cdot polylog(n))$

- Similar approach can be used to get a quadratic speed up in Dynamic programs.

>[!Corollary]
>Size(s) citucits  have Branching programs of size $2^{\tilde{O} (S)}$ where $s = o(n^2)$.

- Space bounded computation can be simulated using Branching programs. 

>[!Corollary] Lower bound
>$\forall s(n) \geq n$, $SPACE(s) \notin TIME(S^2/\log^2 s)$ 

- proof follows from space hierarchy theorem. 

##### $d$-dimensional Turing Machines
- $TIME_d \subset SPACE(t \log t)^{1 - \frac{1}{d+1}}$.
- there can be other geometries on the tapes. 

>[!Proposition]
>If $\rm{TIME}(t) \subseteq \rm{SPACE} (t^\epsilon)$ $\forall \epsilon$, then $\rm{P} \neq \rm{PSPACE}$.  

- Given a MTM $M$,$x$
Assume $t(n) \geq n^2$, $b = \sqrt{t}$

- Partition the tapes in $b$ blocks such that each block has $t/b$ cells.
- Define a DAG $G_{M,x}$: 
	- Node represents "b steps" of time.
	- there will be $t/b$ nodes. 
	- name then $0,1, \dots , t/b$

>[!Observation] 
>- During a time block, $\leq 2$ tape blocks are accessed for each tape. 
>- For $i < j$: put $(i,j)$ if info at time block $i$ needed to compute $j$. 

- state, head positions of all the tapes
- if there exist a tape block visited in time block $i$ and time block $j$ but not accessed in between $i$ and $j$. 
- $in-deg(i) \leq 2k+1$. 



Question: 
- Is this approach useful in the Chronogram?
- Time blocks and Fredman-Saks 

content(0): initial config of M on x -> $O(n)$ bits.
content(i): info computed at time block $i$, i.e. state, all the tape blocks accessed in the time block, head positions. $O(b)$ bits. 

Given content(i), $\forall i: (i,j)$ edge  content (j) in O(b) time. 

Goal: determine content(t/b). 

###### Pebble game 
- DAG $G$ on $n$ nodes.
- put pebble on a source. 
- given pebble on $i$: $(i,j)$ edge can pebble $j$.
- remove a $p$.

Q: How many pebbles to get to last node? 
A: $O(n/\log n)$ for graphs with in-degree $O(1)$. 

Store $O(\frac{t/b}{\log t/b})$ strings of $O(b)$ length. 

### Tree Evaluation Problem(TEP)
- [Braverman, Cook , McKenzie, Santhanam, W.. '09]
studied as a candidate problem to seperate $P$ from Log-Space.  

- For $d,b,h > 0$ 
- $d$-ary tree of height $h$
- each internal node $u$ has function $f_u: \{0,1\}^{db} \to \{0,1\}^b$.
- leaves have $b$-bit string on them. 

Task: Compute the value at the root. 
Input size: $n = 2^{h+b}$ for constant $d$.

Easy: $O(d\cdot h\cdot b)$ space by a DFS. 
- [Cook, Mertz'24] TEP in $O(h \log (db)+ db)$ space.
- In terms of the input length, it is $SPACE(\log n\cdot \log \log n)$. 
	- XOR
	- d registers of b bits 
	  
- [ ] watch Cook and Mertz video on TEP. 
      
Reduce it to a exponential size TEP where the input is not stored explicity but in a succint manner. 

- Assume we know $G_{m,x}$. 
- $b$ such that $\forall i$ |content(i) $\leq b$, $d = 2k+1$, $h = \frac{t}{b} +1$. 

Convert the DAG to a Tree and do a TEP. 

How do we know the graph   
Fix: Make the turing machine nice WLOG.
Oblivious Turing machines $O(t \log t)$. $\forall n$, $x: |x|=n$, the head moves depend only on $n$. [HS'66, PF'79]. Sorting network.  