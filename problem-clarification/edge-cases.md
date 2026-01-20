**Edge Case Sweep**

A systematic pass through the most failure prone input scenarios before coding or finalizing logic. The goal is to break assumptions early, not to prove the happy path works.

**Common sweep categories**

* **Empty**

  * No elements, null, or missing input.
  * Typical failures: index errors, division by zero, incorrect defaults.
  * Question to answer: What should the function return when there is nothing to process?

* **Single**

  * Exactly one element.
  * Typical failures: off by one logic, incorrect initialization.
  * Question to answer: Does the logic still work without iteration?

* **Duplicates**

  * Repeated identical values.
  * Typical failures: incorrect comparisons, overwriting state, assuming uniqueness.
  * Question to answer: Are duplicates allowed and should they affect the result?

* **Extremes**

  * Min or max possible values, very large or very small numbers, boundaries.
  * Typical failures: overflow, underflow, incorrect comparisons.
  * Question to answer: Are numeric or size limits handled safely?

* **Worst ordering**

  * Inputs arranged in the most adversarial order.
  * Examples: sorted ascending or descending, all same value, zigzag patterns.
  * Typical failures: performance degradation, worst case time complexity, recursion depth.
  * Question to answer: Does the algorithm still meet constraints in the worst case?

**Why it matters**

An edge case sweep exposes hidden assumptions. If logic survives these cases, it is usually correct for everything in between.
