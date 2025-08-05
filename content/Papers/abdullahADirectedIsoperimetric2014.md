---
{"publish":true,"title":"A directed isoperimetric inequality with application to bregman near neighbor lower bounds","created":"2025-05-24T17:36:25.786+01:00","modified":"2025-07-07T15:01:53.125+01:00","published":"2025-07-07T15:01:53.125+01:00","cssclasses":""}
---


# A directed isoperimetric inequality with application to bregman near neighbor lower bounds


>[!meta]- Abstract
Bregman divergences are important distance measures that are used in applications such as computer vision, text mining, and speech processing, and are a focus of interest in machine learning due to their information-theoretic properties. There has been extensive study of algorithms for clustering and near neighbor search with respect to these divergences. In all cases, the guarantees depend not just on the data size n and dimensionality d, but also on a structure constant μ ≥ 1 that depends solely on a generating convex function φ and can grow without bound independently. In general, this μ parametrizes the degree to which a given divergence is "asymmetric". In this paper, we provide the first evidence that this dependence on μ might be intrinsic. We focus on the problem of ac{ann} search for Bregman divergences. We show that under the cell probe model, any non-adaptive data structure (like locality-sensitive hashing) for c-approximate near-neighbor search that admits r probes must use space Ω(dn1 + μ/c r). In contrast for LSH under l1 the best bound is Ω(dn1+ 1/cr). Our results interpolate between known lower bounds both for LSH-based ANN under l1 as well as the generally harder Partial Match problem (in non-adaptive settings). The bounds match the former when μ is small and the latter when μ is Ω(d/log n). This further strengthens the intuition that Partial Match corresponds to an "asymmetric" version of ANN, as well as opening up the possibility of a new line of attack for lower bounds on Partial Match. Our new tool is a directed variant of the standard boolean noise operator. We prove a generalization of the Bonami-Beckner hypercontractivity inequality (restricted to certain subsets of the Hamming cube), and use this to prove the desired directed isoperimetric inequality that we use in our data structure lower bound.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/A. Abdullah\|A. Abdullah]], [[people/Suresh Venkatasubramanian\|Suresh Venkatasubramanian]]
> Related:: 
> url:: https://doi.org/10.1145/2746539.2746595
> doi:: 10.1145/2746539.2746595
> bibliography:: Abdullah, A., and Suresh Venkatasubramanian. 2014. ‘A Directed Isoperimetric Inequality with Application to Bregman near Neighbor Lower Bounds’. [https://doi.org/10.1145/2746539.2746595](https://doi.org/10.1145/2746539.2746595).

---
## Self Notes
{% persist "notes" %}
Model::Dynamic  
Problems::[[Problems/Data_Structures/Both/Nearest Neighbour/Nearest Neighbour#^026236\|Bregmen Nearest Approximate Neighbour]]  
Techniques::Directed isoperimetric inequality, hypercontractivity  
lbs::Space lower bound of $\Omega(𝑑𝑛^{(1 + 𝜇/𝑐𝑟)})$ under cell probe model for non-adaptive data structures
model:: cell probe 
where 
- $\mu$ parametrizes the degree to which a given divergence is "asymmetric" 
- $c$ is the approximation factor
- $r$ number of probes.
InorOut: In
{% endpersist %}

## Reading notes
{% persist "annotations" %}
- Problems : papers that study this problem, techniques used to solve this problem 
- Papers : talks about problems studied and techniques applied
- Techniques: Problems studies using the technique, Papers which apply this technique

LB proof: (problem, techniques ,paper) 
{% endpersist %}
