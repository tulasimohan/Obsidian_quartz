$\newcommand{\cX}{\mathcal{X}}$
$\newcommand{\cY}{\mathcal{Y}}$
Richness lemma is an extension of the monochromatic rectangle lower bound for symmetric communication. 
###### Cite: 
- Miltersen, Nisan, Safra, Wigderson 
- Miltersen

###### Define:
- $(u,v)$ richness 
- $[a,b]$ protocol

- [ ] What is the final quantifiable claim about richness? 

###### Theorem 
If $f$ is $(u,v)$-rich and has $Disc(f) \leq bla$, then $f$ does not have an $(s,w,t)$ solution.   
###### Proof. 

>[!lem] Lemma [MNSW]
>If $f$ is $(u,v)$-rich and $f$ has a $[a,b]$ protocol, then $f$ has a $\frac{u}{2^{a+2}} \times \frac{v}{2^{a+b+2}}$ rectangle which is all 1s.   

>[!lem] Lemma [MNSW]
>If $f$ has an $(s,w,t)$ solution then $f$ has a $[2t \log s, 2tw]$ protocol for the corresponding comunication problem.  

>[!Cor] Corollary 
>If $f$ is $(u,v)$ rich and $f$ has an $(s,w,t)$ protocol, then $Disc(f) \geq \frac{uv}{16|\cX||\cY|2^{2t(2 \log S + w)}}$. 

>**Proof.** 

$\frac{uv}{16 \cdot 2^{2a + b}\cdot |\cX||\cY|} = \frac{uv}{16|\cX||\cY|2^{4t \log S + 2tw}}$

Consider $w = \log s$? 

$2^{2(t \log s + 1)} \times 2^{2(t \log s + t w +1)}$ = $4 s^{2t} \times 4^{tw+1}s^{2t}$ = $4 s^{2t} \times 4(2^ws)^{2t}$

Monochromatic rectangle $\frac{u}{4s^{2t}} \times \frac{v}{4(2^ws)^{2t}}$ . 

>What is the Discrepancy of an $r \times s$ monochromatic rectangle in an $m \times n$ table?
Ans: $\frac{rs}{mn}$. 

- Size of the table comes into picture now. 
***

>[!Q] Question 
>What is the richness of a random table?  

- [ ] Compute the richness of a random table. 

>[!Q] Question
>What is the Discrepancy of a random table?  

- [ ] Compute Discrepancy of a Random table.  

- [ ] Argue that the Property is Polytime computable.  

What are these params $u,v, bla,s,w,t$ ? 

A: $f$ is easy. 
B: $f$ is not $(u,v)$ rich. 
C: $f$ has a large monochromatic rectangle.
D: $f$ has large discrepancy.  

- $f$ is $(u,v)$ rich and has small monochromatic rectangles $\implies$ $f$ is hard.  
- $f$ is easy $\implies$ $f$ is not $(u,v)$ rich or $f$ has a large monochromatic rectangle. 
- $f$ is easy $\implies$ $f$ is not $(u,v)$ rich or $f$ has large discrepancy.  

Contrapositive:If $f$ is $(u,v)$-rich and  $f$ has small discrepancy then $f$ is hard.  

$A \implies B \vee C$
$C \implies D$
This implies $A \implies B \vee D?$

Property: $f$ is not $(u,v)$ rich or $f$ has discrepancy  

**$(u,v)$-rich**: 
$v$ columns of the matrix have $u$ ones.  

What is the probability that $f$ is $(u,v)$ rich? 

- Expected number of ones in each column = $\frac{|\cX|}{2} = \mu$
- Let $u = (1+ \delta) \frac{|\cX|}{2} = (1 + \delta) \mu$ ,
- Let the probability that a column has $u$ ones = $p_u$, this can be computed using Chernoff bound. 

- Expected number of columns with $u$ ones =   $p_u|\cX|$
- let $v = (1 + \delta)p_u|\cX|$
- The probability that $v$ columns have $u$ ones:

