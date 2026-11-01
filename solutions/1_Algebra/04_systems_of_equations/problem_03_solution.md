# Systems of Linear Equations

## Question

### Exercise 3. Inconsistent System
Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 2 & \vert & 3 \\
2 & 4 & \vert & 7
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Main Steps:**
  1. Eliminate the entry below the pivot in Column 1 by performing $R_2 \leftarrow R_2 - 2R_1$:
     $$
     \begin{pmatrix}
     1 & 2 & \vert & 3 \\
     2 - 2(1) & 4 - 2(2) & \vert & 7 - 2(3)
     \end{pmatrix} = \begin{pmatrix}
     1 & 2 & \vert & 3 \\
     0 & 0 & \vert & 1
     \end{pmatrix}
     $$

---

### 2. Contradiction in the Matrix and Equation Interpretation

- **Result:**
  - The system is **inconsistent** (no solution exists).

- **Main Steps & Interpretation:**
  1. Translate the second row of the reduced augmented matrix back into an equation:
     $$
     0x + 0y = 1 \implies 0 = 1
     $$
  2. Since $0 = 1$ is a mathematical contradiction, no values of $x$ and $y$ can satisfy both equations simultaneously.
  3. **Algebraic / Geometric Interpretation:** The left-hand sides of the original equations are proportional ($2x + 4y = 2(x + 2y)$), whereas the constants are not proportional ($7 \neq 2 \cdot 3 = 6$). Geometrically, this corresponds to two parallel, distinct lines that never intersect.

- **Explanation & Reasoning:**
  When Gaussian elimination produces a row of zeros on the coefficient side with a non-zero entry on the augmented side (i.e., $[0 \quad 0 \mid c]$ where $c \neq 0$), it signifies an impossible mathematical statement, proving that the system is inconsistent and lacks any solution, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
