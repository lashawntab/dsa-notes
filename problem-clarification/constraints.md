Categorized Constraints

1. Algorithmic Core Constraints
These directly determine time/space complexity and algorithm choice.

| Constraint             | What It Controls              |
| ---------------------- | ----------------------------- |
| Input size (n)         | Feasible time complexity      |
| Value range            | Array vs hash vs tree         |
| Order guarantees       | Binary search, two pointers   |
| Duplicates allowed     | Counting vs set logic         |
| One vs many queries    | Computation vs data structure |
| Streaming input        | Online vs offline algorithms  |
| Static vs dynamic data | Preprocess vs maintain        |
| Mutate input           | In-place vs extra space       |
| Read-only input        | Disallows marking/swapping    |

2. Performance Envelope Constraints
These restrict which solutions will pass in practice.

| Constraint              | What It Controls                   |
| ----------------------- | ---------------------------------- |
| Time limit              | Eliminates slow complexity classes |
| Space limit             | Eliminates memory-heavy approaches |
| Single vs multi-pass    | Feasibility of preprocessing       |
| Single vs multi-machine | Distributed vs local solution      |

3. Behavioral / Correctness Constraints
These affect how the code must behave, not Big O.

| Constraint           | What It Controls              |
| -------------------- | ----------------------------- |
| Pure function        | Side effects allowed or not   |
| Determinism          | Cacheability, reproducibility |
| Precision / overflow | Numeric correctness           |

4. Execution Model Constraints
These appear in real systems more than interviews.

| Constraint             | What It Controls             |
| ---------------------- | ---------------------------- |
| Concurrency            | Immutability or coordination |
| Failure tolerance      | Retries, idempotence         |
| Real-time requirements | Latency vs throughput        |
