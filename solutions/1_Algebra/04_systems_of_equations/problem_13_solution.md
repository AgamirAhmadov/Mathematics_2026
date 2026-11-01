# Systems of Linear Equations

## Question

### Exercise 13. Does Every Equation Add New Information?
Consider the system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

> **Why this exercise:** teaches how to recognize redundant equations within a system.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & 0 & \vert & 10 \\
0 & 1 & 1 & \vert & 8 \\
1 & 0 & -1 & \vert & 2
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Main Steps:**
  1. Eliminate the entry below the pivot in Column 1 by performing $R_3 \leftarrow R_3 - R_1$:
     $$
     \begin{pmatrix}
     1 & 1 & 0 & \vert & 10 \\
     0 & 1 & 1 & \vert & 8 \\
     1 - 1 & 0 - 1 & -1 - 0 & \vert & 2 - 10
     \end{pmatrix} = \begin{pmatrix}
     1 & 1 & 0 & \vert & 10 \\
     0 & 1 & 1 & \vert & 8 \\
     0 & -1 & -1 & \vert & -8
     \end{pmatrix}
     $$
  2. Eliminate the entry in Column 2 of Row 3 by performing $R_3 \leftarrow R_3 + R_2$:
     $$
     \begin{pmatrix}
     1 & 1 & 0 & \vert & 10 \\
     0 & 1 & 1 & \vert & 8 \\
     0 & 0 & 0 & \vert & 0
     \end{pmatrix}
     $$

---

### 2. Parametric Form of the Solution

- **Result:**
  - Free variable: $x_3 = t$ (where $t \in \mathbb{R}$)
  - Parametric solution: $(x_1, x_2, x_3) = (2 + t, 8 - t, t)$

- **Main Steps:**
  1. Translate the row echelon matrix back into equations:
     - Row 2: $x_2 + x_3 = 8 \implies x_2 = 8 - t$
     - Row 1: $x_1 + x_2 = 10 \implies x_1 + (8 - t) = 10 \implies x_1 = 2 + t$
  2. Because Column 3 contains no pivot, variable $x_3$ is a free parameter ($x_3 = t$).

---

### 3. Redundancy Check and Independence Analysis

- **Result:**
  - Not all three equations are independently necessary; **Equation 3 is redundant**.

- **Calculation & Proof of Redundancy:**
  Subtract Equation 2 from Equation 1:
  $$
  (x_1 + x_2) - (x_2 + x_3) = 10 - 8
  $$
  Simplifying the left and right sides yields:
  $$
  x_1 - x_3 = 2
  $$
  This algebraic combination produces **Equation 3** exactly. 

- **Explanation & Reasoning:**
  Because the third equation can be derived directly as a linear combination (the difference) of the first two equations, it does not introduce any new independent geometric constraints. It represents a redundant condition, meaning the solution set is entirely determined by the first two equations, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
