# Determinants and Invertibility

## Question

### Exercise 6. Parameter and Invertibility
For

$$
A(t)=
\begin{pmatrix}
t & 1 \\
2 & t \\
\end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.


## Solution

Let the parameterized matrix $A(t)$ be defined as follows:

$$
A(t) = \begin{pmatrix}
t & 1 \\
2 & t
\end{pmatrix}
$$

---

### 1. Compute $\det A(t)$

- **Result:**
  $$
  \det A(t) = t^2 - 2
  $$

- **Main Steps:**
  1. Apply the standard formula for a $2 \times 2$ determinant ($\det = ad - bc$):
     $$
     \det A(t) = (t)(t) - (1)(2) = t^2 - 2
     $$

---

### 2. Find values of $t$ for which $A(t)$ is not invertible

- **Result:**
  $$
  t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}
  $$

- **Main Steps:**
  1. Set the determinant equal to zero to identify where the matrix becomes singular (non-invertible):
     $$
     \det A(t) = 0 \implies t^2 - 2 = 0
     $$
  2. Solve for $t$:
     $$
     t^2 = 2 \implies t = \pm\sqrt{2}
     $$

---

### 3. Explanation & Theoretical Connection

- **Explanation & Reasoning:**
  A fundamental property of linear algebra states that a square matrix $M$ is **invertible** if and only if its determinant is non-zero:
  $$
  M \text{ is invertible} \iff \det(M) \neq 0
  $$
  
  Conversely, $M$ is **not invertible** (singular) if and only if its determinant equals zero ($\det(M) = 0$).

  When $t = \sqrt{2}$ or $t = -\sqrt{2}$, the rows of $A(t)$ become linearly dependent (one row is a scalar multiple of the other). Geometrically, the linear transformation defined by $A(t)$ collapses 2D space onto a 1D line (zero area), destroying information and making it impossible to reverse (invert) the transformation back to unique initial inputs.
