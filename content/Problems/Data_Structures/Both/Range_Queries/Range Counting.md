

- [ ] define the problem
- [ ] define the parameters 
# Range Counting

>[!DSP] Range Counting
>**Data:** The (exact) range counting problem is to store a set from an ordered universe so that, 
>**Queries:** for any two elements $x \leq x'$ in the universe, the number of elements in the set that are in the range $[x, x']$ can be determined.

## 2D Range Counting

og_lb: [[Lower bounds for 2-dimensional range counting\|Lower bounds for 2-dimensional range counting]]
by Patrascu 2007

- LSD $\to$ 2D Range Counting [[Patrascu Unifying the landscape.canvas|Patrascu Unifying the landscape]]


> [!Note] 2D Range Counting #static_DSP 
  **Data Domain:** Given a set $P$ of $n$ points in the 2D plane and 
  **Query Domain:** a query rectangle $R$ (defined by its bottom-left and top-right corners), 
  $f(x,y)$ the 2D range counting problem asks to determine the number of points in $P$ that lie within $R$.  
  
  This is also sometimes referred to as ***Orthogonal Range Counting***.

### **Upper Bounds:**

* **O(n log n) preprocessing, O(log n) query time:**  Using a 2D range tree.  This is a classic data structure approach.  (Bentley, 1975; Lueker, 1978; Willard, 1978).  Several variations exist with slightly different preprocessing/query tradeoffs.
* **O(n) preprocessing, O(√n) query time:** Using kd-trees.  This offers a good balance, especially for lower dimensions. (Bentley, 1975)
* **O(n log n/log log n) preprocessing, O(log n/log log n) query time (expected):**  Using range trees combined with fractional cascading. (Chazelle and Guibas, 1986).  This represents a slight theoretical improvement over standard range trees.
* **O(m) preprocessing, O(n/√m) query time:** Using the batched range counting technique for *m* queries.  This approach is useful when dealing with many queries at once. (Chazelle, 1988)
* **O(n polylog n) preprocessing, O(logε n) query time (approximate counting):** For a (1+ε)-approximation.  Allows for significantly faster queries at the cost of some error.  (Arya and Mount, 2000)


### **Lower Bounds:**

* **Ω(log n/log log n) query time:**  Under the pointer machine model. (Chazelle, 1990)  This indicates that, up to polylogarithmic factors, the range tree with fractional cascading is close to optimal in this model.
* **Ω(√n) query time (for linear space):**  Under the algebraic decision tree model. (Fredman, 1982) This implies that kd-trees are near-optimal for linear

```mermaid
flowchart LR
    Patrascu --> 2DRC["2D Range Counting"]

```
