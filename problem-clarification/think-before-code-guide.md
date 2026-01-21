# Think Before Code Guide

**Purpose:** Pre-pseudocode problem-solving checklist for DSA problems.

1. Read Problem  
- Carefully read the description, inputs, outputs, and requirements

2. Restate Problem  
- Rewrite the problem in your own words  
- Summarize what needs to be computed or verified  
- Highlight anything unclear or ambiguous

3. Classify Problem  
- Domain/Problem Context: What kind of data? (e.g. Array, String, Tree) — see [domains](domains.md)
- Type/Pattern: Which approach or algorithmic pattern? (e.g. Search, Count, Optimize) — see [patterns](patterns.md)
- Input characteristics: What shape/constraints? (e.g. size, sorted, range) — see [input-characteristics](input-characteristics.md)
- Expected output: What form? (e.g. value, collection, Boolean) — see [output-characteristics](output-characteristics.md)

4. Scope  
- Interview-style → focus on correctness + Big O  
- Production-style → focus on validation + robustness

5. Scale  
- Single machine? → normal algorithms; No → partition, aggregate, minimize network
  - All data fits in memory on one machine.
  - No need to worry about network, communication, or parallel coordination.
  - Runs in memory? → random access ok; No → streaming, chunking
- Multi-machine / distributed
  - Data is too large to fit on one machine or arrives from multiple sources.
  - You need distributed algorithms, like MapReduce: each machine finds a local max, then a global max is computed.
  - Adds complexity: network cost, failure handling, and combining results.

6. Queries ([queries](queries.md))
- One query → direct computation  
- Many queries → Offline: preprocess; Online: indexed structures

7. Constraints ([constraints](constraints.md))
- Algorithmic core constraints
- Performance envelope constraints
- Behavioral and correctness constraints
- Execution model constraints

-- What to focus on when:
 * Interviews Focus almost entirely on Algorithmic core and Performance envelope.
 * System design / production focus on all four sections matter.
 * If not stated assume defaults
    * One query
    * Offline
    * Single machine
    * Mutable input
    * Deterministic

8. Performance Goal ([performance](performance.md)) 
- Latency → Someone is waiting 
- Throughput → Background work
- Consistency vs availability once partitions exist.

9. Complexity Gate ([complexity](complexity.md))
- Time and space

10. Edge Case Sweep ([edge cases](edge-cases.md))
- Input characterization guarantees the legal input set
- Edge case sweep targets the smallest, largest, and most fragile inputs inside that set.
- This is not the same as negative testing or out of bounds.
- e.g. non-empty array (test length = 1)

11. Clarifying Questions & Assumptions  ([clarifying questions](clarifying-questions.md))
- Steps 1–10 surface signals.
- Step 11 is where you lock them in.
- Record all questions you would ask  
- List assumptions and constraints for your approach
- Summarize everything.  ([summary script](pre-coding-summary-verbal-script.md))

12. Outline Solution  
- Only now create verbal plan or pseudocode
