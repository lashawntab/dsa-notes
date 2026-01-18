
Common Type / Patterns
| **Pattern / Type**          | **What It Does**                  | **Typical Use Cases**                    | **Conditions That Qualify This Pattern**                                               |
| --------------------------- | --------------------------------- | ---------------------------------------- | -------------------------------------------------------------------------------------- |
| Linear Scan / Iteration     | One pass, track state             | Find max/min, sum, count                 | Unsorted or unordered input; single query; must check all elements; no preprocessing   |
| Two Pointers                | Coordinated pointer movement      | Sorted arrays, pair sums, palindromes    | Sorted/semi-ordered sequence; looking for pairs or windows; linear traversal possible  |
| Sliding Window              | Maintain moving subarray/window   | Longest/shortest subarray, averages      | Contiguous subarray/subsequence; single-pass; sum or other accumulation constraints    |
| Prefix Sum / Cumulative Sum | Precompute cumulative totals      | Range sum queries                        | Frequent range queries; immutable array; additive operations                           |
| Hash Map / Frequency Count  | Count or complement lookup        | Two-sum, anagrams, duplicates            | Lookup/counting; input unsorted; repeated elements allowed                             |
| Set-based Lookup            | Track seen values                 | Detect duplicates, uniqueness checks     | Duplicates may exist; order doesn’t matter; membership queries                         |
| Stack                       | LIFO processing                   | Expression evaluation, DFS               | Linear sequence; backtracking or temporary storage                                     |
| Queue                       | FIFO processing                   | BFS, simulation                          | Linear or graph traversal; level-order or order-sensitive tasks                        |
| Binary Search               | Halve search space                | Search in sorted array, monotonic answer | Input sorted or monotonic; single-element/index search; monotonic condition            |
| DFS                         | Explore deeply                    | Graphs, trees, backtracking              | Graph/tree input; recursive exploration; path exploration needed                       |
| BFS                         | Level-by-level exploration        | Shortest path, grids                     | Graph/grid input; shortest distance or level-order traversal; unweighted/equal weights |
| Heap / Priority Queue       | Always access extreme efficiently | Top-k, scheduling                        | Repeated min/max queries; dynamic updates; priority-based processing                   |
| Greedy Selection            | Local optimal choice              | Interval scheduling                      | Problem allows locally optimal choices to yield global optimum                         |
| Interval Merge              | Combine overlapping ranges        | Calendar, booking problems               | Ranges or intervals overlap; merging needed                                            |
| Grid DFS / BFS              | Traverse 2D grids                 | Number of islands, flood fill            | Matrix input; neighbor-based traversal; obstacles or paths                             |


Advanced Type / Patterns
| **Pattern / Type**            | **What It Does**                    | **Typical Use Cases**                        | **Conditions That Qualify This Pattern**                                     |
| ----------------------------- | ----------------------------------- | -------------------------------------------- | ---------------------------------------------------------------------------- |
| Kadane / Running Aggregate    | Track best subarray dynamically     | Max subarray sum                             | Maximum/minimum sum in contiguous sequence; negatives allowed                |
| Search on Answer              | Binary search on result space       | Capacity optimization, min time              | Solution space monotonic; answer testable by function; optimization required |
| Divide and Conquer            | Split into subproblems              | Merge sort, recursive calculations           | Problem divisible into independent subproblems; combine results efficiently  |
| 1D Dynamic Programming        | Build solution from previous states | Fibonacci, LIS                               | Optimal substructure; overlapping subproblems                                |
| 2D / Grid Dynamic Programming | DP over matrix cells                | Min path sum, path counting                  | Grid/matrix input; neighbor/state dependencies; optimal substructure         |
| Knapsack DP                   | Optimize under constraints          | Weight/value problems                        | Resource-limited optimization; discrete choices; DP state representable      |
| State Compression DP          | DP with bitmask states              | TSP, subsets                                 | Combinatorial state space; subset states representable as bits               |
| Topological Sort              | Order tasks respecting dependencies | Task scheduling, DAGs                        | DAG input; dependency constraints                                            |
| Union-Find / Disjoint Set     | Track connected components          | Cycle detection, MST                         | Graph connectivity problem; components mergeable; dynamic unions             |
| Shortest Path Algorithms      | Find min-cost paths                 | Dijkstra, Bellman-Ford                       | Weighted graph; path optimization required                                   |
| Monotonic Stack               | Maintain ordered stack invariant    | Next greater/smaller element                 | Need to track increasing/decreasing sequence; linear traversal               |
| Monotonic Queue               | Maintain ordered queue invariant    | Sliding window max/min                       | Need moving window max/min; linear traversal over sequence                   |
| Backtracking                  | Exhaustive search with pruning      | Permutations, Sudoku                         | Combinatorial problem; constraints prune search; recursive exploration       |
| Recursion with Constraints    | DFS with rules                      | Sudoku, word search                          | Graph/tree/grid; constraints limit valid paths; need full exploration        |
| 2D Prefix Sum                 | Precompute cumulative 2D totals     | Submatrix sum queries                        | 2D grid; frequent sum queries; additive operations                           |
| Two Heaps                     | Maintain median dynamically         | Streaming median                             | Streaming input; need median or balanced partitions; dynamic updates         |
| Reservoir Sampling            | Random selection from stream        | Random k elements from large/infinite stream | Unknown or infinite input; uniform random selection required                 |
