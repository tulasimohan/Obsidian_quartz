---
{"publish":true,"title":"Local decodability of the Burrows-Wheeler transform","created":"2025-07-07T17:19:06.984+01:00","modified":"2025-07-07T17:31:26.414+01:00","published":"2025-07-07T17:31:26.414+01:00","cssclasses":""}
---

# Local decodability of the Burrows-Wheeler transform

>[!meta]- Abstract
- The Burrows-Wheeler Transform (BWT) is among the most influential discoveries in text compression and DNA storage. 
It is a reversible preprocessing step that rearranges an $n$-letter string into runs of identical characters (by exploiting context regularities), resulting in highly compressible strings, and is the basis of the &lt;pre&gt;bzip&lt;/pre&gt; compression program. 
Alas, the decoding process of BWT is inherently sequential and requires $Ω(n)$ time even to retrieve a single character. 
- We study the succinct data structure problem of locally decoding short substrings of a given text under its compressed BWT, i.e., with small additive redundancy r over the Move-To-Front (&lt;pre&gt;bzip&lt;/pre&gt;) compression. 
- The celebrated BWT-based FM-index (FOCS ’00), as well as other related literature, yield a trade-off of $r=Õ(n/\sqrt{t})$ bits, when a single character is to be decoded in $O(t)$ time. 
- We give a near-quadratic improvement $r=Õ(n\lg(t)/t)$. As a by-product, we obtain an exponential (in t) improvement on the redundancy of the FM-index for counting pattern-matches on compressed text. 
- In the interesting regime where the text compresses to $o(n)$ (say, n/polylg(n)) bits, these results provide an exp(t) overall space reduction. For the local decoding problem of BWT, we also prove an $Ω(n/t^2)$ cell-probe lower bound for “symmetric” data structures.
- We achieve our main result by designing a compressed partial-sums (Rank) data structure over BWT. The key component is a locally-decodable Move-to-Front (MTF) code: with only O(1) extra bits per block of length nΩ(1), the decoding time of a single character can be decreased from $Ω(n)$ to $O(\lg n)$. 
  This result is of independent interest in algorithmic information theory.

> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/9J4ECYAB)
> Authors:: [[people/Sandip Sinha\|Sandip Sinha]], [[people/Omri Weinstein\|Omri Weinstein]], 
> Related:: 
> url:: https://dl.acm.org/doi/10.1145/3313276.3316317
> doi:: 
> bibliography:: Sinha, Sandip, and Omri Weinstein. 2019. “Local Decodability of the Burrows-Wheeler Transform.” In _Proceedings of the 51st Annual ACM SIGACT Symposium on Theory of Computing_, 744–55. STOC 2019. New York, NY, USA: Association for Computing Machinery. [https://doi.org/10.1145/3313276.3316317](https://doi.org/10.1145/3313276.3316317).

---
## My Notes


model:: Static
techniques:: non-uniform version of [[Techniques/Static/Cell elimination\|Cell elimination]] technique
problems::  Local decoding of Burrow Wheeler Transform, [[Succint Permutations]] Problem
lbs:: 

- [ ] Looks like a reduction from Succint premutations problem and the lb is like $\tilde{\Omega}(\log n)$ lower bound.
- [ ] Techniques look interesting. 
- [ ] To read. 




