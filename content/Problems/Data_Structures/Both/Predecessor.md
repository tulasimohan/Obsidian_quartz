---
{"publish":true,"created":"2025-05-24T17:36:31.003+01:00","modified":"2025-07-07T15:16:17.164+01:00","published":"2025-07-07T15:16:17.164+01:00","cssclasses":""}
---

# Static Predecessor

- [ ] Define the parameters. 

M:: $\binom{n}{m} 2^\ell$
N:: $n$

>[!Note] $P(n,m)$ 
>- $D$ = $y \subseteq U$ where $U = \{0, \dots n-1\}$ and $|y|=m$
>- $Q$ = $x\in U$.
>- $f(x,y)$ what is $\max\{z \in y | z \leq x\}$?

$M = 2^{n}$ or $\binom{n}{m}= O(n^m)$,  $N = n$
where $M$ is the number of data points and $N$ is the number of queries.

- LB: [[../../Papers/ajtaiLowerBoundFinding1988\|Ajtai 1988]] proved a super constant lower bound. 
- LB: [[../../Papers/miltersenLowerBoundsUnionSplitFind1994\|Miltersen 1994]] $\Omega(\sqrt{\log \log n})$
- LB: [[../../Papers/miltersenDataStructuresAsymmetric1998\|Miltersen 1998]]   $\Omega((\log m)^{1/3})$. 
- LB: [[../../Papers/beameOptimalBoundsPredecessor2002\|Beame & Fich 2002]] come up with a matching upper and lower bound.
- LB: [[../../Papers/patrascuTimespaceTradeoffsPredecessor2006\|Patrascu 2006]] showed a lower bound when space $S = O(n\log^{O(1)}n)$. 

Ajtai and Xiao obtained the same bound independently. 

| Paper                                                                                           | Lower bound on $t$                             |
| ----------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| [[Papers/ajtaiLowerBoundFinding1988\|ajtaiLowerBoundFinding1988]]                               | super constant                                 |
| Xiao '92                                                                                        | super constant                                 |
| [[Papers/miltersenLowerBoundsUnionSplitFind1994\|miltersenLowerBoundsUnionSplitFind1994]]       | $\Omega(\sqrt{\log \log n})$                   |
| [[Papers/miltersenDataStructuresAsymmetric1998\|miltersenDataStructuresAsymmetric1998]]         | $\Omega((\log m)^{1/3})$                       |
| [[Papers/beameOptimalBoundsPredecessor2002\|beameOptimalBoundsPredecessor2002]]                 | $\Omega(\frac{\log \log n}{\log \log \log n})$ |
| [[Papers/patrascuTimespaceTradeoffsPredecessor2006\|patrascuTimespaceTradeoffsPredecessor2006]] |                                                |

>**Quote**
>The static predecessor problem concerns the representation of a subset A of the universe $U = \{1,2,\cdots,u\}.$  The operations supported are queries "find the largest element in A that is less than or equal to $i\in\ U$".
>We extend results of M. Ajtai to show that any implementation of such a problem with space bounded by poly($\vert A\vert$) and poly($\log\ u$) word size requires $\Omega({\log\ \log\ u\over\log\ \log\ \log\ u})$ probes to answer a query in the worst case. The same lower bound is also proved for the dynamic predecessor problem in which the space restriction is dropped and the update operations are added."


Upper bounds For Static Predecessor
- [[../../Notes/Van Emde Boas trees\|Van Emde Boas trees]]:  $O(\log \log n)$ time using $\Omega(n)$ space. 
- [[../../Papers/beameOptimalBoundsPredecessor2002\|Beame & Fich 2002]] : $\min (\frac{\log \log n}{\log \log \log n}, \sqrt{\frac{\log m}{\log \log m}})$ 


## Dynamic Predecessor

[[../../Papers/beameOptimalBoundsPredecessor2002\|Beame & Fich 2002]] Beame and Fich prove a $\Omega(\sqrt{\log m/\log \log m})$ lower bound in the dynamic setting.

Upper bounds For Dynamic Predecessor
- Using Anderson and Thorup's reduction from Dynamic to Static [[../../Papers/beameOptimalBoundsPredecessor2002\|Beame & Fich 2002]] 
	$O(\min\{\frac{[\log \log n}{\log \log \log n}\log \log m , \sqrt{\frac{\log m}{\log \log m}}\})$
