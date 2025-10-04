---

## 📊 1. Analysis of Algorithms
- **Definition**: The process of determining the efficiency of an algorithm in terms of time and space.
- **Why it matters**: Two algorithms may solve the same problem, but one could be 100× faster or use far less memory.
- **Key aspects**:
  - **Time Complexity** → How execution time grows with input size.
  - **Space Complexity** → How much memory is required.
  - **Correctness** → Does it always produce the right result?
  - **Scalability** → How it behaves as input grows very large.

---

## 🔁 2. Analysis of Common Loops & Recursion
### Loops
- **Single loop**:  
  cpp
  for (int i = 0; i < n; i++) { ... }
  
  → Runs **n times** → **O(n)**.
- **Nested loop**:  
  cpp
  for (int i = 0; i < n; i++) {
      for (int j = 0; j < n; j++) { ... }
  }
 
  → Runs **n × n = n² times** → **O(n²)**.
- **Dependent loop**:  
 cpp
  for (int i = 0; i < n; i++) {
      for (int j = 0; j < i; j++) { ... }
  }
 
  → Runs **1 + 2 + … + n ≈ n²/2** → **O(n²)**.

### Recursion
- **Example**: Factorial  
  cpp
  int fact(int n) {
      if (n == 0) return 1;
      return n * fact(n-1);
  }
 
  - Each call reduces `n` by 1 → **n calls** → **O(n)**.
- **Divide & Conquer Example**: Merge Sort  
  - Splits array into halves → recurrence:  
    $$T(n) = 2T(n/2) + O(n)$$  
    → Solves to **O(n log n)**.

---

## ∞ 3. Asymptotic Notation
Used to describe performance as input size → ∞.

- **Big-O (O)** → *Upper bound* (worst case).  
  Example: Linear search → **O(n)**.
- **Big-Ω (Ω)** → *Lower bound* (best case).  
  Example: Linear search (if element is first) → **Ω(1)**.
- **Big-Θ (Θ)** → *Tight bound* (average case).  
  Example: Linear search → **Θ(n)**.

---

## 💾 4. Space Complexity
- **Definition**: Total memory used by an algorithm.
- **Components**:
  - **Fixed part** → constants, program code, etc.
  - **Variable part** → input data, recursion stack, dynamic allocations.
- **Examples**:
  - Iterative Fibonacci → **O(1)** space.
  - Recursive Fibonacci → **O(n)** space (due to call stack).

---

## 📈 5. Order of Growth
- **Definition**: How runtime grows relative to input size.
- **Common orders**:
  | Growth | Example | Efficiency |
  |--------|---------|------------|
  | O(1)   | Accessing array element | Excellent |
  | O(log n) | Binary search | Very good |
  | O(n)   | Linear search | Good |
  | O(n log n) | Merge sort | Efficient |
  | O(n²)  | Bubble sort | Poor for large n |
  | O(2ⁿ)  | Recursive subset generation | Very poor |
  | O(n!)  | Traveling salesman brute force | Impractical |

---

✅ **Quick mental model**:  
- Loops → count iterations.  
- Recursion → write recurrence relation.  
- Asymptotics → ignore constants & small terms.  
- Space → track variables + recursion depth.  
- Order of growth → compare how fast functions blow up.

---

# ⚡ DSA Analysis Cheat Sheet

## 1. Analysis of Algorithms
- **Goal**: Measure efficiency in **time** and **space**.
- **Focus**:  
  - Time Complexity → growth of execution steps.  
  - Space Complexity → memory usage.  
  - Correctness & scalability.

---

## 2. Common Loop Patterns
| Code Pattern | Iterations | Complexity |
|--------------|------------|------------|
| `for (i=0; i<n; i++)` | n | **O(n)** |
| Nested: `for (i=0; i<n; i++) for (j=0; j<n; j++)` | n × n | **O(n²)** |
| Dependent: `for (i=0; i<n; i++) for (j=0; j<i; j++)` | 1+2+…+n ≈ n²/2 | **O(n²)** |
| Doubling: `for (i=1; i<n; i*=2)` | log₂n | **O(log n)** |

---

## 3. Recursion Analysis
- **Method**: Write recurrence relation.
- **Examples**:
  - Factorial:  
    $$T(n) = T(n-1) + O(1) \implies O(n)$$
  - Merge Sort:  
    $$T(n) = 2T(n/2) + O(n) \implies O(n \log n)$$
  - Fibonacci (naïve recursion):  
    $$T(n) = T(n-1) + T(n-2) + O(1) \implies O(2^n)$$

---

## 4. Asymptotic Notation
- **Big-O (O)** → Worst-case upper bound.  
- **Big-Ω (Ω)** → Best-case lower bound.  
- **Big-Θ (Θ)** → Tight bound (average case).  

👉 Ignore constants & lower-order terms.  
Example: `3n² + 5n + 10 → O(n²)`.

---

## 5. Space Complexity
- **Components**:
  - Fixed part → constants, code.  
  - Variable part → input, recursion stack, dynamic memory.
- **Examples**:
  - Iterative Fibonacci → O(1).  
  - Recursive Fibonacci → O(n) (stack depth).  
  - Merge Sort → O(n) (extra arrays).

---

## 6. Order of Growth (Hierarchy)
| Growth | Example | Practicality |
|--------|---------|--------------|
| O(1)   | Array access | Excellent |
| O(log n) | Binary search | Very good |
| O(n)   | Linear search | Good |
| O(n log n) | Merge/Quick sort | Efficient |
| O(n²)  | Bubble/Insertion sort | Poor for large n |
| O(2ⁿ)  | Recursive subsets | Impractical |
| O(n!)  | Brute-force TSP | Impossible for large n |

---

## 🔑 Quick Rules of Thumb
- **Loop count = time complexity.**
- **Recursion = recurrence relation.**
- **Drop constants & small terms.**
- **Space = variables + recursion depth.**
- **Compare growth rates to judge scalability.**

---
