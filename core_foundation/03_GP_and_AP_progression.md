---

## 🔹 Arithmetic Progression (AP)
An **Arithmetic Progression** is a sequence of numbers where the **difference between consecutive terms is constant**.

### General Form
```
a, a + d, a + 2d, a + 3d, … 
```
- **a** = first term  
- **d** = common difference  

### nth Term Formula
\[
a_n = a + (n-1)d
\]

### Sum of First n Terms
\[
S_n = \frac{n}{2} \big[2a + (n-1)d\big]
\]
or equivalently,
\[
S_n = \frac{n}{2}(a + l)
\]
where **l** is the last term.

✅ **Example**:  
AP = 3, 7, 11, 15, …  
- Here, \(a = 3\), \(d = 4\).  
- 5th term: \(a_5 = 3 + (5-1) \cdot 4 = 19\).  
- Sum of first 5 terms: \(S_5 = \frac{5}{2}[2\cdot3 + (5-1)\cdot4] = 55\).

---

## 🔹 Geometric Progression (GP)
A **Geometric Progression** is a sequence where each term is obtained by **multiplying the previous term by a constant ratio**.

### General Form
```
a, ar, ar², ar³, …
```
- **a** = first term  
- **r** = common ratio  

### nth Term Formula
\[
a_n = a \cdot r^{n-1}
\]

### Sum of First n Terms
If \(r \neq 1\):
\[
S_n = \frac{a(r^n - 1)}{r - 1}
\]

If \(r = 1\):
\[
S_n = n \cdot a
\]

### Sum of Infinite GP
If \(|r| < 1\):
\[
S_\infty = \frac{a}{1-r}
\]

✅ **Example**:  
GP = 2, 6, 18, 54, …  
- Here, \(a = 2\), \(r = 3\).  
- 4th term: \(a_4 = 2 \cdot 3^{3} = 54\).  
- Sum of first 4 terms: \(S_4 = \frac{2(3^4 - 1)}{3 - 1} = 80\).

---

## 🔑 Why AP & GP Matter in DSA
- **AP** shows up in problems involving **linear growth** (e.g., sum of first n natural numbers, distributing tasks, loop iterations).  
- **GP** shows up in problems involving **exponential growth** (e.g., binary trees, powers of 2, compound interest, algorithm complexity like O(log n)).  
- Many **mathematical tricks** in coding contests rely on quickly recognizing AP/GP patterns to avoid brute force.

---

⚡ Quick DSA Connection:
- **AP**: Sum of first n natural numbers → \(n(n+1)/2\).  
- **GP**: Number of nodes in a complete binary tree of height h → \(2^{h+1} - 1\).  

---


---

# 📘 AP & GP Cheat Sheet (DSA Reference)

---

## 🔹 Arithmetic Progression (AP)

**Definition:** Sequence with a constant difference between consecutive terms.  

**General Form:**  
\[
a, \; a+d, \; a+2d, \; a+3d, \dots
\]

- **a** = first term  
- **d** = common difference  

### Key Formulas
- **nth term:**  
  \[
  a_n = a + (n-1)d
  \]

- **Sum of first n terms:**  
  \[
  S_n = \frac{n}{2}[2a + (n-1)d] \quad \text{or} \quad S_n = \frac{n}{2}(a + l)
  \]

- **Special Cases:**  
  - Sum of first n natural numbers: \(\; \frac{n(n+1)}{2}\)  
  - Sum of first n odd numbers: \(\; n^2\)  
  - Sum of first n even numbers: \(\; n(n+1)\)

### DSA Applications
- Loop iteration counts  
- Time complexity analysis (linear growth)  
- Problems involving distributing items evenly  
- Detecting linear patterns in arrays  

---

## 🔹 Geometric Progression (GP)

**Definition:** Sequence with a constant ratio between consecutive terms.  

**General Form:**  
\[
a, \; ar, \; ar^2, \; ar^3, \dots
\]

- **a** = first term  
- **r** = common ratio  

### Key Formulas
- **nth term:**  
  \[
  a_n = a \cdot r^{n-1}
  \]

- **Sum of first n terms (r ≠ 1):**  
  \[
  S_n = \frac{a(r^n - 1)}{r - 1}
  \]

- **Sum of infinite GP (|r| < 1):**  
  \[
  S_\infty = \frac{a}{1-r}
  \]

### DSA Applications
- Binary trees (nodes count = \(2^{h+1}-1\))  
- Exponential growth problems (e.g., doubling, halving)  
- Algorithm complexity (divide & conquer → log n)  
- Compound interest, probability problems  

---

## 🔑 Quick Comparison Table

| Feature              | Arithmetic Progression (AP) | Geometric Progression (GP) |
|----------------------|------------------------------|-----------------------------|
| Rule                 | Add constant \(d\)          | Multiply by constant \(r\)  |
| nth term             | \(a + (n-1)d\)              | \(a \cdot r^{n-1}\)         |
| Sum of n terms       | \(\frac{n}{2}[2a+(n-1)d]\)  | \(\frac{a(r^n-1)}{r-1}\)    |
| Growth type          | Linear                      | Exponential                 |
| DSA use cases        | Loops, linear sums          | Trees, powers, complexity   |

---

## ⚡ Pro Tips for Contests
- Memorize **AP sums** for natural, odd, and even numbers.  
- Recognize **GP patterns** in binary trees, recursion, and logarithmic complexity.  
- When stuck, check if the sequence is **linear (AP)** or **exponential (GP)**.  
- For large n, use **modular arithmetic** (common in coding contests).  

---

