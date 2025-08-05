---
{"publish":true,"title":"Coarse-grained complexity for dynamic algorithms","created":"2025-05-24T17:36:28.371+01:00","modified":"2025-07-07T23:07:29.498+01:00","published":"2025-07-07T23:07:29.498+01:00","cssclasses":""}
---


# Coarse-grained complexity for dynamic algorithms


>[!meta]- Abstract
To date, the only way to argue polynomial lower bounds for dynamic algorithms is via fine-grained complexity arguments. 
These arguments rely on strong assumptions about specific problems such as the Strong Exponential Time Hypothesis (SETH) and the Online Matrix-Vector Multiplication Conjecture (OMv). 
While they have led to many exciting discoveries, dynamic algorithms still miss out some benefits and lessons from the traditional "coarse-grained" approach that relates together classes of problems such as P and NP. 
In this paper we initiate the study of coarse-grained complexity theory for dynamic algorithms. 
Below are among questions that this theory can answer. 
What if dynamic Orthogonal Vector (OV) is easy in the cell-probe model? 
A research program for proving polynomial unconditional lower bounds for dynamic OV in the cell-probe model is motivated by the fact that many conditional lower bounds can be shown via reductions from the dynamic OV problem (e.g. [Abboud, V.-Williams, FOCS 2014]). 
Since the cell-probe model is more powerful than word RAM and has historically allowed smaller upper bounds (e.g. [Larsen, Williams, SODA 2017; Chakraborty, Kamma, Larsen, STOC 2018]), it might turn out that dynamic OV is easy in the cell-probe model, making this research direction infeasible. 
Our theory implies that if this is the case, there will be very interesting algorithmic consequences: 
If dynamic OV can be maintained in polylogarithmic worst-case update time in the cell-probe model, then so are several important dynamic problems such as 
>- k-edge connectivity, 
>- (1 + ϵ)-approximate mincut, 
>- (1 + ϵ)-approximate matching, 
>- planar nearest neighbors, 
>- Chan's subset union and 
>- 3-vs-4 diameter. 
>The same conclusion can be made when we replace dynamic OV by, e.g., subgraph connectivity, single source reachability, Chan's subset union, and 3-vs-4 diameter. 
>Lower bounds for k-edge connectivity via dynamic OV? The ubiquity of reductions from dynamic OV raises a question whether we can prove conditional lower bounds for, e.g., 
>- k-edge connectivity, 
>- approximate mincut, and 
>- approximate matching, via the same approach. 
> Our theory provides a method to refute such possibility (the so-called non-reducibility). In particular, we show that there are no "efficient" reductions (in both cell-probe and word RAM models) from dynamic OV to k-edge connectivity under an assumption about the classes of dynamic algorithms whose analogue in the static setting is widely believed. We are not aware of any existing assumptions that can play the same role. (The NSETH of Carmosino et al. [ITCS 2016] is the closest one, but is not enough.) To show similar results for other problems, one only need to develop efficient randomized verification protocols for such problems.

> [!meta]- Metadata
> zotero_link:: 
> Authors:: [[people/Sayan Bhattacharya\|Sayan Bhattacharya]], [[people/Danupon Nanongkai\|Danupon Nanongkai]], [[people/Thatchaphol Saranurak\|Thatchaphol Saranurak]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Bhattacharya, Sayan, Danupon Nanongkai, and Thatchaphol Saranurak. 2020. ‘Coarse-Grained Complexity for Dynamic Algorithms’. [https://doi.org/10.1137/1.9781611975994.29](https://doi.org/10.1137/1.9781611975994.29).


---
## My Notes

Model::Dynamic  
Problems::[[Problems/Data_Structures/Static/Orthogonal Vector Counting]], [[k-edge connectivity]], [[$(1 + \epsilon)$-approximate mincut]], [[$(1 + \epsilon)$-approximate matching]], [[planar nearest neighbors]], [[Chan's subset union]] and [[3-vs-4 diameter]].
Techniques:: reductions  
lbs:: Conditional lbs assuming hardness of some problems(completeness type of results). 
InorOut:: Out




