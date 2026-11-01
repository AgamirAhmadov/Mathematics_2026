# Systems of Linear Equations

## Question

### Exercise 8. Two Systems with the Same Coefficient Matrix
Solve by elimination the two systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.


## Solution

---

### 1. Solve System 1

- **Augmented Matrix Setup:**
  $$
  [A \mid b_1] = \begin{pmatrix}
  2 & 1 & \vert & 5 \\
  1 & -1 & \vert & 1
  \end{pmatrix}
  $$

- **Row Reduction:**
  1. Swap Row 1 and Row 2 to place a convenient pivot ($1$) in the top-left position ($R_1 \leftrightarrow R_2$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 1 \\
     2 & 1 & \vert & 5
     \end{pmatrix}
     $$
  2. Eliminate the entry below the pivot ($R_2 \leftarrow R_2 - 2R_1$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 1 \\
     0 & 3 & \vert & 3
     \end{pmatrix}
     $$
  3. Scale Row 2 ($R_2 \leftarrow \frac{1}{3}R_2$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 1 \\
     0 & 1 & \vert & 1
     \end{pmatrix}
     $$

- **Back-Substitution & Solution 1:**
  - From Row 2: $y = 1$
  - From Row 1: $x - (1) = 1 \implies x = 2$
  - **Result:** $(x, y) = (2, 1)$

---

### 2. Solve System 2

- **Augmented Matrix Setup:**
  $$
  [A \mid b_2] = \begin{pmatrix}
  2 & 1 & \vert & 1 \\
  1 & -1 & \vert & 4
  \end{pmatrix}
  $$

- **Row Reduction:**
  1. Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 4 \\
     2 & 1 & \vert & 1
     \end{pmatrix}
     $$
  2. Eliminate the entry below the pivot ($R_2 \leftarrow R_2 - 2R_1$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 4 \\
     0 & 3 & \vert & -7
     \end{pmatrix}
     $$
  3. Scale Row 2 ($R_2 \leftarrow \frac{1}{3}R_2$):
     $$
     \begin{pmatrix}
     1 & -1 & \vert & 4 \\
     0 & 1 & \vert & -\frac{7}{3}
     \end{pmatrix}
     $$

- **Back-Substitution & Solution 2:**
  - From Row 2: $y = -\frac{7}{3}$
  - From Row 1: $x - \left(-\frac{7}{3}\right) = 4 \implies x + \frac{7}{3} = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}$
  - **Result:** $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$

---

### 3. Comparison of Elimination Steps and Explanation

- **What is the Same:**
  - All elementary row operations applied to the **coefficient matrix $A$** (the row swap, row scaling factors, and row addition multiples) are **100% identical** in both systems. 
  - The resulting matrix structure on the left side of the vertical bar prior to back-substitution is identical in both cases.

- **Explanation & Reasoning:**
  - Because both systems share the exact same coefficient matrix $A = \begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix}$, the left-hand side coefficients govern the underlying linear transformation (or lines intersecting in 2D space) independently of the constant terms. 
  - The right-hand side vectors ($b_1$ and $b_2$) merely track how the constants are transformed alongside the rows. This separation demonstrates why matrix factorization (like LU decomposition) is so powerful: we can factor or reduce the coefficient matrix once and apply it to multiple distinct right-hand side vectors efficiently, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
