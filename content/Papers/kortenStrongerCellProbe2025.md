---
{"publish":true,"title":"Stronger Cell Probe Lower Bounds via Local PRGs","created":"2025-05-24T17:36:28.021+01:00","modified":"2025-07-07T14:31:55.457+01:00","published":"2025-07-07T14:31:55.457+01:00","cssclasses":""}
---


# Stronger Cell Probe Lower Bounds via Local PRGs


>[!meta]- Abstract
In this work we observe a tight connection between three topics: NC0 cryptography, NC0 range avoidance, and static data structure lower bounds. Using this connection, we leverage techniques from the cryptanalysis of NC0 PRGs to prove state-of-the-art results in the latter two subjects. Our main result is a quadratic improvement to the best known static data structure lower bounds, breaking a barrier which has stood for several decades. Prior to our work, the best known lower bound for any explicit problem with M inputs and N queries was SNt1(logM)1−t1 for any setting of the word length w (where S= space and t= time) (Siegel ‘89). We prove, for the same class of explicit problems considered by Siegel, a quadratically stronger lower bound of the form SNt2(logM)1−t22−O(w)  for all even t0. Second, for the restricted class of nonadaptive bit probe data structures, we improve on this lower bound polynomially: for all odd constants t1 we give an explicit problem with N queries and MNO(1) inputs and prove a lower bound S(Nt2+t) for some constant t0. Our results build off of an exciting body of work on refuting semi-random CSPs.
We then utilize our explicit cell probe lower bounds to obtain the best known unconditional algorithms for NC0 range avoidance: we can solve any instance with stretch nm in polynomial time once mnt2 when t is even; with the aid of an NP oracle we can solve any instance with mnt2−t for t0 when t is odd. Finally, using our main correspondence we establish novel barrier results for obtaining significant improvements to our cell probe lower bounds: (i) near-optimal space lower bounds for an explicit problem with t=4w=1  implies EXPNPNC1 ; (ii) under the widely-believed assumption that polynomial-stretch NC0 PRGs exist, there is no natural proof of a lower bound of the form SN(1) when t=(1), w=1.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/WZNR625P)
> Authors:: [[people/Oliver Korten\|Oliver Korten]], [[people/Toniann Pitassi\|Toniann Pitassi]], [[people/Russell Impagliazzo\|Russell Impagliazzo]], 
> Related:: 
> url:: https://eccc.weizmann.ac.il/report/2025/030/
> doi:: 
> bibliography:: Korten, Oliver, Toniann Pitassi, and Russell Impagliazzo. 2025. ‘Stronger Cell Probe Lower Bounds via Local PRGs’. Electronic Colloquium on Computational Complexity. [https://eccc.weizmann.ac.il/report/2025/030/](https://eccc.weizmann.ac.il/report/2025/030/).

---
## My Notes






