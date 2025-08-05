---
{"publish":true,"title":"Bloom filter","created":"2025-05-24T17:36:33.965+01:00","modified":"2025-05-24T17:36:30.947+01:00","published":"2025-05-24T17:36:30.947+01:00","cssclasses":""}
---


#data_structure  #set-membership

- Allows false positive but not any false negatives
- cannot remove an item from a Bloom-filter
- [[ LSM tree]]
- uses [[Hash functions]]

Let $f_i: [n] \to [m]$ $i \in [k]$ be a collection of hash functions.

- **Insertion**: A bloom filter  maintains an array of length $m$ initialised to all zeroes. 
When an element $x$ is inserted into our set, the bloom filter sets the locations given by $f_i(x) \forall i \in [k]$ to 1.
- **Membership** of an element $x$ is checked by probing the locations given by $f_i(x) \forall i \in [k]$ and checking if they are all 1. 

## NotebookLM
1. **What is the primary problem addressed in Bloom's paper?**
1A. Ans SetMembership when the universe-size is much larger than the set size. 

2. **What are the three computational factors considered in the analysis of hash coding methods?**
The three factors are 
 - space (size of the hash area), 
 - reject time (time to identify a non-member), and 
 - allowable error frequency.
 
3. **How do conventional hash coding methods differ from the new methods proposed by Bloom?**
 Conventional methods aim for error-free identification, requiring larger hash areas. Bloom's methods allow a small fraction of errors to significantly reduce space requirements.

4. **Describe the key characteristics of applications where Bloom suggests his new hash coding methods would be beneficial.**
Ideal applications involve testing a large number of cases where most are simple to process, and a small, hard-to-identify minority require a more complex process.

5. **Briefly explain the mechanism of Method 1 in reducing hash area size.**
   Method 1 uses smaller cells containing codes derived from the messages instead of storing entire messages. The code size is determined by the permissible error fraction.
   
6. **How does Method 2 deviate from the traditional concept of organizing a hash area?**
Method 2 treats the hash area as individual addressable bits. Each message sets a specific number of bits to 1, and membership is determined by checking if all corresponding bits are set.

7. **Define the normalized time measure (T) used in Bloom's analysis.**
T is the average time to reject a message, measured in units of time needed to calculate a bit address, access the bit, and test its contents.

8. **What is the significance of the variable 'E' in the analysis of the conventional hash coding method?**
 'E' represents the expected number of bits tested before recognizing a mismatch in a non-empty cell during a rejection procedure.
 
9.  **Explain how the allowable fraction of errors (P') is calculated in Method 1.**
   P' is calculated as the probability of a non-member message having the same hash-generated code as a member and that code being encountered before an empty cell.

10. **What is the relationship between the normalized time measure (T") and the fraction of 0 bits in the hash field (ф") in Method 2?**
T" is inversely proportional to ф". A higher T" implies a lower ф" (fewer 0 bits), meaning more bits are set to 1, increasing the chance of false positive identifications.

