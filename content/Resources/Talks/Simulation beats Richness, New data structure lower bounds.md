---
{"publish":true,"title":"Mukhopadhyay@Simulation beats richness","created":"2018","modified":"2025-05-24T17:36:31.139+01:00","published":"2018","cssclasses":""}
---

#talk

(s,w,t) problem

##### Matrix vector product


A randomized asymmetric simulation theorem


***Asymmetric communication:***
	Alice has a bigger input than Bob.
	$O(a,b)$ protocol: Alice sends $a$ bits and Bob sends $b$ bits. 
	$\Omega(a,b)$ protocol: Alice needs to send $\geq a$ bits or Bob needs to send $\geq b$ bits. 

>[!claim] 
$(s,w,t)$ protocol $\implies$ $(tw,t\log s)$ protocol. 

##### Richness technique
by Peter Bro Miltersen
- Membership MEM
- Subspace membership SUB-MEM
- lopsided Set-Disj

$[u,v]$ rich:= there are $v$ columns each of which have at least $u$ ones.  

#richness 

>[!lem] [Miltersen '95]
>If $f$ is $[u,v]$ rich and has a $(a,b)$ protocol $\implies$ $\exists$ a large i.e. $(\frac{u}{2^a},\frac{v}{2^{a+b}})$ mono-chromatic rectangle.

#### Asymmetric Simulation or Lifting theorem

***Composed function***

$f \circ g(X,Y)$ :=  $f(g(X_1,Y),\ldots , g(X_p,Y))$

$g = IP_n \implies f \circ MVP_{p \times n}$ 


##### Deterministic simulation theorem (Asymmetric)

>***Upper bound for $f_p \circ MVP_{p \times n}$ :*** 
>$\cc(f\circ MVP) = O(\pdt(f)\cdot n, \pdt(f))$ 

>***A matching lower bound:*** 
>$\cc(f\circ MVP) = \Omega(\pdt(f)\cdot n, \pdt(f))$ 

>***Lower bound in the randomized setting:*** 
>$\rcc(f\circ MVP) = \Omega(\rpdt(f) \cdot n,\rpdt(f))$


##### Beating Richness
Give a promise problem for which richness method does not work.

>***1 -inputs***: $2n$ length
>- 0 in even positions.
>- $\geq \frac{n}{10}$ 1s in the odd positions.
>***0-inputs***: $2n$ length
>- 0 in odd position 
>- $\geq \frac{n}{10}$ 1s in the even positions. 

- This function has and efficient Randomized query complexity. 
- This gives a Randomized Zero error $CC$ protocol for $F\circ MVP_{n \times n}$.
- By standard truncation technique, we get a 1-sided error protocol.

>[!Note] 
> Richness technique also gives a 1-sided error protocol. 

- This problem has a small 1-sided error protocol so richness doesn't work. 
- This problem has large Parity decision tree complexity so lifting works for proving lbs.
$\newcommand{\pdt}{D^{\oplus dt}}$
$\newcommand{\rpdt}{R^{\oplus dt}}$
$\newcommand{\cc}{D^{CC}}$
$\newcommand{\rcc}{R^{CC}}$
