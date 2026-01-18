| **Characteristic**      | **What It Means**                   | **Why It Matters / Implications**                                     |
| ----------------------- | ----------------------------------- | --------------------------------------------------------------------- |
| Size (n)                | Number of elements                  | Determines time complexity limits                                     |
| Sorted                  | Input is sorted or partially sorted | Enables binary search, two pointers                                   |
| Unsorted                | No ordering guarantee               | Forces linear scan or hashing                                         |
| Unique                  | No duplicates                       | Simplifies logic, allows sets                                         |
| Contains Duplicates     | Repeated values possible            | Requires counting or frequency tracking                               |
| Fixed Length            | Size does not change                | Allows indexing assumptions                                           |
| Dynamic Length          | Insertions/deletions allowed        | May require linked structures                                         |
| Read-only               | Input cannot be modified            | Disallows in-place solutions                                          |
| Mutable                 | Input can be changed                | Allows marking, swapping, in-place                                    |
| Single Pass             | Input streamed once                 | Requires online algorithms                                            |
| Multiple Passes Allowed | Can revisit input                   | Enables preprocessing or offline algorithms                           |
| One Query               | Compute answer once                 | Simpler algorithms acceptable                                         |
| Many Queries            | Repeated queries                    | Preprocessing or caching becomes valuable                             |
| Bounded Values          | Known min/max                       | Enables counting sort, arrays                                         |
| Unbounded Values        | No numeric limits                   | Requires hashing, trees, or other flexible structures                 |
| Dense                   | Most possible values present        | Arrays efficient                                                      |
| Sparse                  | Few values present                  | Maps or sparse structures better                                      |
| Weighted                | Values have costs                   | Requires DP or shortest path                                          |
| Unweighted              | All costs equal                     | BFS often sufficient                                                  |
| Cyclic                  | Input may contain cycles            | Requires visited tracking                                             |
| Acyclic                 | No cycles                           | Simplifies traversal                                                  |
| Grid / Matrix           | 2D structure                        | Neighbor-based traversal patterns                                     |
| Graph                   | Nodes and edges                     | DFS, BFS, shortest path                                               |
| Tree                    | Hierarchical, acyclic               | Recursive patterns apply                                              |
| Offline                 | Full input known                    | Allows preprocessing, sorting, multiple passes; can optimize globally |
| Online                  | Input arrives piece by piece        | Requires incremental updates, single-pass, and often O(1) memory      |
