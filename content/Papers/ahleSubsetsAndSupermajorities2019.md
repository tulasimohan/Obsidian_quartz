---
{"publish":true,"title":"Subsets and supermajorities Optimal hashing-based set similarity search","created":"2025-05-24T17:36:28.303+01:00","modified":"2025-07-07T14:31:55.458+01:00","published":"2025-07-07T14:31:55.458+01:00","cssclasses":""}
---


# Subsets and supermajorities Optimal hashing-based set similarity search


>[!meta]- Abstract
We formulate and optimally solve a new generalized 
**Set Similarity Search problem**, which assumes the size of the database and query sets are known in advance. By creating polylog copies of our data-structure, 
we optimally solve any symmetric Approximate Set Similarity Search problem, including approximate versions of Subset Search, Maximum Inner Product Search (MIPS), Jaccard Similarity Search, and Partial Match. 
Our algorithm can be seen as a natural generalization of previous work on Set as well as Euclidean Similarity Search, but conceptually it differs by optimally exploiting the information present in the sets as well as their complements, and doing so asymmetrically between queries and stored sets. 
Doing so we improve upon the best previous work: MinHash [J. Discrete Algorithms 1998], SimHash [STOC 2002], Spherical LSF [SODA 2016, 2017], and Chosen Path [STOC 2017] by as much as a factor n<sup>{</sup>0.14} in both time and space; or in the near-constant time regime, in space, by an arbitrarily large polynomial factor. 
Turning the geometric concept, based on Boolean supermajority functions, into a practical algorithm requires ideas from branching random walks on {Z}<sup>{</sup>2}, for which we give the first non-asymptotic near tight analysis. Our lower bounds follow from new hypercontractive arguments, which can be seen as characterizing the exact family of similarity search problems for which supermajorities are optimal. The optimality holds for among all hashing based data structures in the random setting, and by reductions, for 1 cell and 2 cell probe data structures.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Thomas Dybdahl Ahle\|Thomas Dybdahl Ahle]], [[people/Jakob Bæk Tejs Knudsen\|Jakob Bæk Tejs Knudsen]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Ahle, Thomas Dybdahl, and Jakob Bæk Tejs Knudsen. 2019. ‘Subsets and Supermajorities: Optimal Hashing-Based Set Similarity Search’. [https://doi.org/10.1109/FOCS46700.2020.00073](https://doi.org/10.1109/FOCS46700.2020.00073).

---
## My Notes

Model::Static  
Problems:: [[Problems/Data_Structures/Static/Partial Match\|Partial Match]] , Approximate [[Problems/Data_Structures/Static/Similarity Search\|Set Similarity Search]] (Subset Search, MIPS, Jaccard)  
Techniques::Boolean supermajority functions, branching random walks  
lbs::Improves MinHash/SimHash lower bounds by polynomial factors
InorOut: Out
Upper bound



