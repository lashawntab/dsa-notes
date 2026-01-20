Performance

- You choose latency vs throughput first.
- CAP only explains what breaks when the network does.

| Dimension         | No Partition Assumed                      | Partition Present, AP Bias    | Partition Present, CP Bias |
| ----------------- | ----------------------------------------- | ----------------------------- | -------------------------- |
| Primary goal      | Latency or throughput on happy path       | Stay available                | Preserve correctness       |
| Latency           | Optimized via local work, no coordination | Low, stable responses         | High, spikes or timeouts   |
| Throughput        | Increased via batching and amortization   | High effective throughput     | Reduced by coordination    |
| Request handling  | Single node or fast fan out               | Serve immediately             | Block, retry, or fail      |
| Writes            | Immediate local execution                 | Accept locally                | Require quorum or leader   |
| Replication       | Not relevant                              | Async, deferred               | Synchronous, coordinated   |
| Data correctness  | Assumed consistent                        | Stale or conflicting possible | Strong, single view        |
| Metrics to watch  | p95, p99 latency or ops/sec               | Error rate, divergence        | Timeout rate, tail latency |
| Decision scope    | Design time optimization                  | Runtime per operation         | Runtime per operation      |


Latency or Throughput on critical/happy path

| Question               | If YES, someone is waiting                         | If NO, nobody is waiting                                  |
| ---------------------- | -------------------------------------------------- | --------------------------------------------------------- |
| Primary choice         | Latency                                            | Throughput                                                |
| What matters           | One request                                        | Many requests                                             |
| Failure interpretation | Slow = broken                                      | Slow is acceptable                                        |
| Optimization focus     | Single operation, critical path                    | Aggregate work, batching                                  |
| Techniques             | Avoid batching and coordination                    | Batch, amortize, async                                    |
| What to measure        | Tail latency (p95, p99)                            | Ops per second, sustained throughput                      |
| Typical examples       | Page load, search results, play button, API call   | Event ingestion, logging, metrics, offline processing,    |
|                        | in request chain                                   | recommendations precomputation                            |

CAP theorem
When a partition occurs, you can choose consistency or availability, not both.

**C — Consistency**

* Every read returns the most recent write or an error.
* All nodes observe the same data at the same time.
* Requires coordination, quorums, or a leader.

**A — Availability**

* Every request receives a non error response.
* The response may not contain the latest data.
* System continues operating even if some nodes are unreachable.

**P — Partition Tolerance**

* The system continues operating despite network splits or dropped messages.
* Messages between nodes can be delayed or lost.
* This is not optional in real distributed systems.

Combinations:
| CAP Type                                    | What it Does                                                                                                             | Use Case                                                                           | Examples                                              |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------- | ----------------------------------------------------- |
| **CP (Consistency + Partition Tolerance)**  | Prioritizes correct data over uptime. During partitions, requests may fail to avoid inconsistency.                       | Financial apps, inventory, payments—anywhere incorrect data is worse than downtime | MongoDB (strict), Apache HBase, Redis, Google Spanner |
| **AP (Availability + Partition Tolerance)** | Prioritizes uptime over strict correctness. During partitions, nodes stay active but may return stale/inconsistent data. | Social media feeds, analytics, CDNs—eventual consistency is acceptable             | Amazon DynamoDB, Apache Cassandra, CouchDB            |
| **CA (Consistency + Availability)**         | Ensures all nodes see the same data and remain responsive—but only works if there are no partitions.                     | Single-node or tightly coupled systems; not realistic in true distributed systems  | MySQL, PostgreSQL (non-distributed)                   |



**Critical clarifications people get wrong**

* Availability does not mean uptime or SLAs.
* Consistency does not mean correctness of business logic, it means read after write visibility.
* Partition tolerance does not mean “handles load”, it means “handles network failure”.

