## Question

### Exercise 2. Formula for a 2×2 Matrix
Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.


## Solution

To find the inverse of a $2 \times 2$ matrix using the explicit formula, we use the standard inverse formula for a matrix of the form $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$:

$$
A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
$$

where $ad - bc$ is the determinant of matrix $A$. If the determinant is non-zero, the matrix is invertible.

---

### 1. Identify Elements and Compute the Determinant

- **Given Elements:**
  $a = 3$, $b = 2$, $c = 5$, $d = 4$

- **Determinant Calculation:**
  $$
  \det(A) = ad - bc = (3)(4) - (2)(5) = 12 - 10 = 2
  $$

- **Explanation & Reasoning:**
  The determinant scales the inverse. Because $\det(A) = 2 \neq 0$, the inverse exists.

---

### 2. Apply the $2 \times 2$ Inverse Formula

- **Calculation:**
  Swap the diagonal elements ($a$ and $d$), negate the off-diagonal elements ($b$ and $c$), and multiply by $\frac{1}{\det(A)}$:
  $$
  A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}
  $$

- **Result:**
  $$
  A^{-1} = \begin{pmatrix} 
  2 & -1 \\ 
  -\frac{5}{2} & \frac{3}{2} 
  \end{pmatrix}
  $$

---

### 3. Verification using Matrix Multiplication

- **Calculation ($A A^{-1}$):**
  $$
  A A^{-1} = \begin{pmatrix}
  3 & 2 \\
  5 & 4
  \end{pmatrix}
  \begin{pmatrix}
  2 & -1 \\
  -\frac{5}{2} & \frac{3}{2}
  \end{pmatrix}
  = \begin{pmatrix}
  (3)(2) + (2)\left(-\frac{5}{2}\right) & (3)(-1) + (2)\left(\frac{3}{2}\right) \\
  (5)(2) + (4)\left(-\frac{5}{2}\right) & (5)(-1) + (4)\left(\frac{3}{2}\right)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  A A^{-1} = \begin{pmatrix}
  6 - 5 & -3 + 3 \\
  10 - 10 & -5 + 6
  \end{pmatrix}
  = \begin{pmatrix}
  1 & 0 \\
  0 & 1
  \end{pmatrix} = I
  $$

- **Explanation & Reasoning:**
  Multiplying the original matrix $A$ by our computed inverse $A^{-1}$ yields the identity matrix $I$, which successfully verifies that the formula was applied correctly and the solution is accurate.
