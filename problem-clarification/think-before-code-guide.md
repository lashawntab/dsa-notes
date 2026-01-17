# Think Before Code Guide

**Purpose:** Pre-pseudocode problem-solving checklist for DSA problems.

1. Read Problem  
- Carefully read the description, inputs, outputs, and requirements

2. Restate Problem  
- Rewrite the problem in your own words  
- Summarize what needs to be computed or verified  
- Highlight anything unclear or ambiguous

3. Classify Problem  
- Domain: Array, String, Tree, Graph, Heap, Linked List, Matrix  
- Type/Pattern: Search, Count, Optimize, Transform, Validate, Substructure, Path  
- Input characteristics: Size, Sorted/Unsorted, Duplicates allowed?, Range, Negative numbers  
- Expected output: Single value, Collection, Boolean, Subsequence

4. Scope  
- Interview-style → focus on correctness + Big O  
- Production-style → focus on validation + robustness

5. Scale  
- Single machine? → normal algorithms; No → partition, aggregate, minimize network  
- Runs in memory? → random access ok; No → streaming, chunking

6. Queries  
- One query → direct computation  
- Many queries → Offline: preprocess; Online: indexed structures

7. Constraints  
- Mutate input? → in-place vs copy  
- Pure function? → no side effects  
- Concurrency? → immutability or coordination

8. Performance Goal  
- Latency → optimize single operation  
- Throughput → batch or amortize

9. Complexity Gate  
- n ≤ 10⁴ → O(n²) acceptable  
- n ≤ 10⁵ → O(n log n)  
- n ≥ 10⁶ → O(n) or streaming

10. Edge Case Sweep  
- Empty, Single, Duplicates, Extremes, Worst ordering

11. Clarifying Questions & Assumptions  
- Record all questions you would ask  
- List assumptions and constraints for your approach

12. Outline Solution  
- Only now create verbal plan or pseudocode
