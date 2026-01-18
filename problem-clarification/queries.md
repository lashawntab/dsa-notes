One Query vs Many Queries

| Category           | One Query                          | Many Queries                         |
| ------------------ | ---------------------------------- | ------------------------------------ |
| What it means      | Function is evaluated once         | Function is evaluated repeatedly     |
| Typical examples   | Given an input, compute the result | Result requested multiple times      |
|                    | Input used once, then discarded    | Result requested after updates       |
| Default assumption | Yes                                | No, must be stated                   |
| Core approach      | Direct computation                 | Structured or maintained computation |
| Time complexity    | Single full computation            | Depends on preprocessing or updates  |
| Space complexity   | Minimal extra space                | Extra space usually required         |
| Preprocessing      | None                               | Often worthwhile                     |
| Online vs offline  | Either is fine                     | Choice depends on data behavior      |

Implications by Data Behavior (Many Queries)
| Data Behavior  | Strategy             | Typical Techniques                         |
| -------------- | -------------------- | ------------------------------------------ |
| Static data    | Preprocess once      | Tables, indexes, segment trees             |
| Dynamic data   | Maintain structure   | Heaps, balanced trees, incremental updates |
| Streaming data | Incremental tracking | Running aggregates                         |

Decision Rule Table
| Step | Question                                       | Outcome                      |
| ---- | ---------------------------------------------- | ---------------------------- |
| 1    | Is the input consumed once and discarded?      | Yes → One query              |
| 2    | Will the function be requested multiple times? | Yes → Many queries           |
| 3    | Does the input change between requests?        | No → Preprocess              |
|      |                                                | Yes → Maintain incrementally |
