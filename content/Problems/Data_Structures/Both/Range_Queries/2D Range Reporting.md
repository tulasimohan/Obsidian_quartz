
- [ ] define the parameters $M$, $N$.
 
The 2D range reporting problem involves preprocessing 

**Data:** a set $P$ of $n$ points in the plane to efficiently answer queries of the form: report all points contained within a given axis-aligned rectangle $R$ (i.e., a range query).  More formally:

>[!dsp] 2D Range Reporting 
**Data:** A set $P$ of $n$ points in the plane.
**Query:** Given an axis-aligned rectangle $R = [x_1, x_2] × [y_1, y_2]$, report all points $(x, y) \in P$ such that $x_1 \leq x \leq  x_2$ and $y_1 \leq  y \leq  y_2$.
**function:** state the upper and lower bounds of 2D range reporting with years of publications

>[!lemma] 
## 2D Range Reporting

2D range reporting queries aim to report all points within a given rectangular region in a 2D space.  Several data structures and algorithms exist with varying performance characteristics, leading to different upper and lower bounds.  These bounds are typically expressed in terms of:

* **N:** The number of points in the dataset.
* **K:** The number of points reported within the query range.
* **n:**  Sometimes used interchangeably with N, but occasionally refers to the size of the input (e.g., if points have associated values).
* **Preprocessing time:** The time required to build the data structure.
* **Space complexity:** The amount of memory used by the data structure.
* **Query time:** The time required to answer a single range query.


Here's a breakdown of some key results, along with approximate years of publication:

### **Lower Bounds:**

* **Ω(log n + K):**  This is a widely accepted lower bound for query time in the pointer machine model [early 1980s].  Essentially, you need logarithmic time to locate the relevant part of the data structure and then linear time proportional to the number of points reported.  This lower bound assumes that points are stored using pointers and accessed sequentially.  Variations of this lower bound exist depending on the specific computational model.


### **Upper Bounds (Data Structures and Algorithms):**

* **Range Trees (1980s):**
    * Preprocessing: O(N log N)
    * Space: O(N log N)
    * Query: O(log² N + K)  (Can be improved to O(log N + K) with fractional cascading)

* **kd-trees (1975):**
    * Preprocessing: O(N log N)
    * Space: O(N)
    * Query: O(√N + K) in worst case, O(log N + K) on average (average case is highly data-dependent and doesn't hold for all distributions)

* **Priority Search Trees (1985):**  Optimized for semi-infinite range queries (e.g., x1 ≤ x ≤ x2, y ≤ y2).
    * Preprocessing: O(N log N)
    * Space: O(N