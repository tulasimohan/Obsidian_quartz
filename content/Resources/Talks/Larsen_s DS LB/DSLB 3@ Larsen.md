---
{"publish":true,"created":"2018","modified":"2025-05-24T17:36:31.164+01:00","published":"2018","cssclasses":""}
---

## Encoding 

Use the data structure to encode $f(S,t)$ and decode for data compression.

#### Polynomial evaluation

Data: degree $n-1$ univariate polynomials over $F_p$ for $p = O(n^2)$.
Queries: $x \in F_p$. 

$f(S,t) \geq n \log p$ 

##### Miltersen's proof as an encoding argument
proof inspired by [Gal, Miltersen 07]  [Golinsky 09]  [Panigrahy rt al 10]

- Encoding $P$
	- Build a data-structure(encoding of $P$) on $P$.
	- For each sequence of $t$-cells, count how many of these queries are going to be answered by probing these $t$ cells. 
	- Let $c_1^*, \dots , c_t^*$ be the cells which encode the most number of queries.
	- the encoding stores the addresses of these cells and their contents. 