BigO Notation - How does it grow?  (Upper bound)

- Growth is measured with respect to input size.
- Asymptotic efficiency compares behavior as input becomes large.
- One algorithm is better if it eventually runs faster for large inputs.
- Loops determine growth, nested loops multiply cost.
- Constants are ignored.
- Analyze the worst case, not best or average.

Why we only use Worst case?

- Average case: Hard to compute, requires knowing input distributions and frequencies, rarely practical.
- Best case: Not useful, a lower bound gives no guarantee on real performance.
- Worst case: Easier to analyze and gives a meaningful upper bound, the standard for evaluating algorithms.

Time Complexity

| Big O      | Name         | Typical Meaning                     | Common Examples                  |
| ---------- | ------------ | ----------------------------------- | -------------------------------- |
| O(1)       | Constant     | No growth with input size           | Array access, variable update    |
| O(log n)   | Logarithmic  | Shrinks problem each step           | Binary search, balanced tree ops |
| O(√n)      | Sublinear    | Faster than linear, slower than log | Trial division, block search     |
| O(n)       | Linear       | One full pass                       | Scan, reduce, map                |
| O(n log n) | Linearithmic | Sort + scan behavior                | Merge sort, heap sort            |
| O(n²)      | Quadratic    | All pairs                           | Nested loops over same input     |
| O(n³)      | Cubic        | Triple nesting                      | Naive matrix multiply            |
| O(nᵏ)      | Polynomial   | Fixed-degree nesting                | DP with k dimensions             |
| O(2ⁿ)      | Exponential  | Doubles per element                 | Subset generation                |
| O(n!)      | Factorial    | Permutations                        | Traveling salesman brute force   |


Space Complexity - Measures additional memory beyond the input.

| Big O    | What It Usually Means              |
| -------- | ---------------------------------- |
| O(1)     | Fixed number of variables          |
| O(log n) | Recursion depth on balanced divide |
| O(n)     | Auxiliary array, stack, map        |
| O(n²)    | Matrix, DP table                   |
| O(2ⁿ)    | Storing all subsets                |
| O(n!)    | Storing all permutations           |


 Rule of Thumb - Decisions

| Complexity           | Practical Interpretation               |
| -------------------- | -------------------------------------- |
| O(1), O(log n), O(n) | Acceptable at scale                    |
| O(n log n)           | Standard for sorting and similar tasks |
| O(n²)                | Risky beyond ~10⁴                      |
| O(2ⁿ), O(n!)         | Only viable for very small n           |

Common mistakes

| Mistake                          | Reality                 |
| -------------------------------- | ----------------------- |
| Counting input size as space     | Input space is excluded |
| Assuming recursion is O(1) space | Call stack counts       |
| Forgetting dominant term         | Lower terms are ignored |
| Mixing time and space            | Analyze separately      |

Tip:

The input list itself is not counted as extra space.
