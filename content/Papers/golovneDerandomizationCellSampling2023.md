---
{"publish":true,"title":"Derandomization of Cell Sampling","created":"2025-05-24T17:36:28.396+01:00","modified":"2025-07-11T13:22:35.866+01:00","published":"2025-07-11T13:22:35.866+01:00","cssclasses":""}
---


# Derandomization of Cell Sampling


>[!meta]- Abstract
Since 1989, the best known lower bound on static data structures was Siegel's classical cell sampling lower bound. Siegel showed an explicit problem with n inputs and m possible queries such that every data structure that answers queries by probing $t$ memory cells requires space . In this work, we improve this bound for non-adaptive data structures to  for all $t ≥ 2$.For $t = 2$, we give a lower bound of $s > m — o (m)$, improving on the bound $s > m/2$ recently proved by Viola over $𝔽_2$ and Siegel's bound  over other finite fields.* The full version of the paper can be accessed at https://arxiv.org/abs/2108.05970

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/WCLRKVRK)
> Authors:: [[people/Alexander Golovne\|Alexander Golovne]], [[people/Tom Gur\|Tom Gur]], [[people/Igor Shinkar\|Igor Shinkar]], 
> Related:: 
> url:: https://epubs.siam.org/doi/10.1137/1.9781611977585.ch26
> doi:: 
> bibliography:: Golovne, Alexander, Tom Gur, and Igor Shinkar. 2023. ‘Derandomization of Cell Sampling’. In _2023 Symposium on Simplicity in Algorithms (SOSA)_, 278–84. Proceedings. Society for Industrial and Applied Mathematics. [https://doi.org/10.1137/1.9781611977585.ch26](https://doi.org/10.1137/1.9781611977585.ch26).

$\newcommand{\F}{\mathbb{F}}$

---
## Self Notes


For Data structure problems of the form $f: \F^n \times [m] \to \F$

Model:: Static
problems:: $k$-wise independent problems for $k= n/\log n$. 
Techniques:: [[Techniques/Static/Cell Sampling\|Cell Sampling]]
lbs:: $s = \tilde{\Omega}(n(\frac{m}{n})^{1/(t-1)})$ improving Siegel's bound $s = \tilde{\Omega}(n(\frac{m}{n})^{1/t})$



## Reading notes



  



