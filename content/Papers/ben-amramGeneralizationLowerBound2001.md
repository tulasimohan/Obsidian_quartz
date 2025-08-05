---
{"publish":true,"title":"A generalization of a lower bound technique due to Fredman and Saks","created":"2025-05-24T17:36:28.038+01:00","modified":"2025-07-11T13:25:27.989+01:00","published":"2025-07-11T13:25:27.989+01:00","cssclasses":""}
---


# A generalization of a lower bound technique due to Fredman and Saks


>[!meta]- Abstract
>In a seminal paper of 1989, Fredman and Saks proved lower bounds for some important datastructure problems in the cell probe model. In particular, lower bounds were established on worst-case and amortized operation cost for the union-find problem and the prefix sum problem. The goal of this paper is to turn their proof technique into a general tool that can be applied to different problems and computational models. To this end we define two quantities: Output Variability depends only on the model of computation. It indicates how much variation can be found in the results of a program with certain resource bounds. This measures in some sense the power of a model. Problem Variability characterizes in a similar sense the difficulty of the problem. Our Main Theorem shows that by comparing a model’s output variability to a problem’s problem variability, lower bounds on the complexity of solving the problem on the given model may be inferred. The theorem thus shows how to separate the analysis of the model of computation from that of the problem when proving lower bounds. We show how the results of Fredman and Saks fit our framework by computing the output variability of the cell probe model and the problem variability for problems considered in their paper. This allows us to reprove their lower bound results, and slightly extend them. The main purpose of this paper though is to present the generalized technique.


> [!meta]- Metadata
> zotero_link:: [Full Text PDF](zotero://select/groups/5902932/items/RGVL6UCQ)
> Authors:: [[people/Amir M. Ben-Amram\|Amir M. Ben-Amram]], [[people/Zvi Galil\|Zvi Galil]], 
> Related:: 
> url:: 
> doi:: 
> bibliography:: Ben-Amram, Amir M., and Zvi Galil. 2001. ‘A Generalization of a Lower Bound Technique Due to Fredman and Saks’. _Algorithmica_ 30 (1): 34–66. [https://doi.org/10.1007/s004530010077](https://doi.org/10.1007/s004530010077).

---
## My Notes

Model::Dynamic  
Problems:: [[Problems/Data_Structures/Dynamic/Partial Sums\|Prefix sums]], [[Problems/Data_Structures/Dynamic/Union-Find\|Union-Find]]  
Techniques::Generalized [[Techniques/Dynamic/Chronogram]] method  
lbs::
InorOut:: out

*Output Variability* depends only on the model of computation. It indicates how much variation can be found in the results of a program with certain resource bounds.

*Problem Variability* characterizes in a similar sense the difficulty of the problem.









