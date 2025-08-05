What is Round elimination ?

Cite all the paper suing Round elimination  

- Probability amplification technique originated in Ajtai's paper
- Useful in both KW games and Cell probe lower bounds

[[Transdichotomous bound]] ?

Round elimination gives a lb on the static  [[Problems/Data_Structures/Both/Predecessor\|Predecessor]] problem $(n^{O(1)}, w , (\log n)^{1/3})$. 
Beame and Finch have the best bound of $\Omega\left(  \sqrt{\frac{\log n}{ \log \log n}} \right)$ .  

- Given $f: X \times  Y \to A$, we can construct $f^{(r)}: X^r \times Y \times [r]\to A$ as follows:
  For all $x_1, \dots , x_r \in X$,  $y \in Y$ and $i \in [r]$,  
$$f^r(x_1, \dots ,x_r,y,i) = f(x_i,y)$$
###### Round elimination lemma
$\exists$ universal constants $R,c$ such that the following holds.   
If there is a $[t,a,b]^A$ protocol for $f^{Ra}$, then there is a $[t-1,ca, cb]^B$ protocol for $f$ 

>[!def] $Col(b,n)$ 
>- Alice gets $x \in \{0, . . . , 2b − 1\}$. 
>- Bob gets gets $S \subseteq \{0, . . . , 2b − 1\}$, where $|S| \leq n$. 
>- Each element of $S$ has an associated colour, either red or blue. They must decide the colour of $\max \{y ∈ S|y ≤ x\}$ . 

how to split a page in obsidian


***



**Step 1:** 

```mehrmaid
graph LR
	AB1["$[t,a,w]^A$ for $col(b,n)$"]
	BA1["$[t,a,w]^A$ for $col[\frac{b}{ca},n]^{(ca)}$"]
	BA2["$[t,a,w]^B$ for $col[b,n]$"]
	AB2["$[t,a,w]^B$ for $^{cb}col[b - \log cb, \frac{n}{cb}]$"]	
	subgraph 1B
		direction LR
	    BA2 --> AB2;
	end
	subgraph 1A
		direction LR
	    AB1 --> BA1;
	end    
```

**Step 2:** 

```mehrmaid
graph LR
	ab1["$[t,a,w]^A$ for $f^{Ra}$"]
	ba1["$[t-1,ca,cw]^B$ for $f$"]
	ba2["$[t,a,w]^B$ for $^{Ra}f$"]
	ab2["$[t-1,ca,cw]^A$ for $f$"]
	subgraph 2B
		direction LR
	    ba2 --> ab2;
	end
	subgraph 2A
		direction LR
	    ab1 --> ba1;
	end    
```



- A $[t,a,b]^A$ protocol for $col[b,n]$ can be converted to a protocol $[t,a,b]^A$ for $col[\frac{b}{ca},n]^{ca}$.

- A $[t,a,b]^B$ protocol for $col[b,n]$ can be converted into a $[t,a,b]^B$ protocol for $^{cb}col[b- \log cb, \frac{n}{cb}]$. 



```mehrmaid
graph LR
	AB1["$[t,a,w]^A$ for $col(b,n)$"]
	BA1["$[t,a,w]^A$ for $col[\frac{b}{ca},n]^{(ca)}$"]
	BA2["$[t,a,w]^B$ for $col[b,n]$"]
	AB2["$[t,a,w]^B$ for $^{cb}col[b - \log cb, \frac{n}{cb}]$"]
	ab1["$[t,a,w]^A$ for $f^{Ra}$"]
	ba1["$[t-1,ca,cw]^B$ for $f$"]
	ba2["$[t,a,w]^B$ for $^{Ra}f$"]
	ab2["$[t-1,ca,cw]^A$ for $f$"]
	
	subgraph 2
		direction LR
	    AB1 --Projection A--> BA1;
	    ab1 --Round Elimination A--> ba1;
	    BA2 --Projection B--> AB2;
		ba2 --Round Elimination B--> ab2;
	end        
```






```mehrmaid
graph TD
    A["$[t, a, w]^{A}$ for $col[b, n]$"]
    B["$[t, a, w]^{A}$ for $col[\frac{b}{ca}, n]^{(ca)}$"]
    C["$[t−1, ca, cw]^{B}$ for $col[\frac{b}{ca}, n]$"]
    D["$[t−1, ca, cw]^{B}$ for $^{(c^2w)}col[\frac{b}{ca} − log(c^2w), \frac{n}{c^2w}]$"]
    E["$[t−2, c^2a, c^2w]^{A}$ for $col[\frac{b}{ca} − log(c^2w), \frac{n}{c^2w}]$"]

    A --1A--> B
    B --2A--> C
    C --1B--> D
    D --2B--> E
    E --loop--> A
```

##### At the end of one cycle of reductions, 
starting from $[t,a,w]^A$ for $col[b,n]$, we get $[t-2,c^2a,c^2w]^A$ for $col[\frac{b}{ca} − log(c^2w), \frac{n}{c^2w}]$.  

How are the Projection and Round elimination steps implemented? 

- Original Ajtai's proof is more ammenable to Random functions than the round elimination.
- What are the limitations of round elimination? 
- This proof has a simulation of proof. "Round elimination is simulation for self reducible functions". 
- Also goes by the name "Probability Amplification". 
#### Projection 
Uses some sort of self reducibility
#### Round elimination 
Does not use anything about the function.

