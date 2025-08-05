---
{"publish":true,"title":"Clifford@Lower bounds for streaming problems","created":"2025-05-24T17:36:35.456+01:00","modified":"2025-05-24T17:36:31.054+01:00","published":"2025-05-24T17:36:31.054+01:00","cssclasses":""}
---

#talk

- Cell probe model

Type 1: Static DS - only queries 
Type 2: Dynamic DS - updates and queries 
Type 3:  Streaming - only updates and just 1 query

## Data structure lower bounds 

Cell probe model - Minsky and Pappert/ Yao (1978) 
### Static 

| Authors                            | Venue         | year |                           |
| ---------------------------------- | ------------- | ---- | ------------------------- |
| Ajtai                              | Combinatorica | 1988 | #communication_complexity |
| Miltersen                          | STOC          | 1994 |                           |
| Miltersen, Nisan, Safra, Wigderson | STOC          | 1995 |                           |
| Beame, Fich                        | STOC          | 1999 |                           |
| Sen                                | ICALP         | 2001 |                           |

#predecessor_search 

### Dynamic 

| Authors                                  | Venue        | year |                       |
| ---------------------------------------- | ------------ | ---- | --------------------- |
| Fredman,Saks                             | STOC         | 1989 | #chronogram_technique |
| Ben-Amran, Galil                         | FOCS         | 1991 |                       |
| Miltersen, Subramanian, Vitter, Tamassia | TCS          | 1994 |                       |
| Husfeldt, Rauhe, Skyum                   | SWAT         | 1996 | planar_connectivity   |
| Fredman, Henzinger                       | Algorithmica | 1998 | #non-determinism      |
| Alstrup, Husfeldt, Rauhe                 | FOCS         | 1998 | #marked_ancestor      |
| Alstrup, Hisfeldt, Rauhe                 | SODA         | 2001 | #2D_NN                |
| Alstrup, Ben-Amram, Rauhe                | STOC         | 1999 | #union_find           |
| Patrascu, Demaine                        | SODA         | 2004 | #information_transfer |

#partial_sums

## Streaming

#multiplication 

>[!note] Problem 1 
>***Online Multiplication*** 
>Input : A stream of pairs of digits arrive
>Output: digits of their product

Time lower bound : $\Omega(\frac\delta w\cdot n \log n)$

M.S. Paterson, M.J. Fischer and A.R. Meyer

>[!note] Problem 2
>***Online Convolution*** / Cross-correlation


- Construct random input distribution and prove a lower bound on deterministic algorithms according to this distribution. 
#### Previous bounds

###### Lower bounds
technique:: Yao's minimax
Lower bound is like $\log n$. 
###### Upper bounds
- M.J.Fischer and L.J.Stockmeyer
  Fast on-line integer multiplication
  STOC'73

- R.Clifford, K.Effermenko, B.Porat, E.Porat
  A black box for online approximate pattern matching
  Information and Computation 2009 
  
- General online to offline reduction to show upper bounds for a large class of problems.  

- Their General method: 
  online-answer = offline-answer $\times \frac{\log n}{n}$. 

- Upper bounds in Streaming imply lower bounds cell probe model.  

- Better online lower bound $\implies$ super-linear lower bound for offline convolution and multiplication. 

##### Information transfer 

Introduced by Kasper Green Larsen in streaming.  ????

> [!note] Information transfer
Memory cells written in the time-period before, read  in this period and written in-between. 

The conditional entropy

- Toepliz matrix

