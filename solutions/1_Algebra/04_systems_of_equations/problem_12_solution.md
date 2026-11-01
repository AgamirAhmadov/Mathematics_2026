# Systems of Linear Equations

## Question

### Exercise 12. Homogeneous System
Solve

$$
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0,0,0)$ always satisfies a homogeneous system.

> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.


## Solution

Let the augmented matrix $[A \mid 0]$ for the given homogeneous system be:

$$
[A \mid 0] = \begin{pmatrix}
1 & 2 & -1 & \vert & 0 \\
2 & 4 & -2 & \vert & 0 \\
1 & -1 & 2 & \vert & 0
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Main Steps:**
  1. Eliminate entries below the pivot in Column 1: perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
     $$
     \begin{pmatrix}
     1 & 2 & -1 & \vert & 0 \\
     0 & 0 & 0 & \vert & 0 \\
     0 & -3 & 3 & \vert & 0
     \end{pmatrix}
     $$
  2. Swap $R_2$ and $R_3$ to place the non-zero row in row echelon form ($R_2 \leftrightarrow R_3$):
     $$
     \begin{pmatrix}
     1 & 2 & -1 & \vert & 0 \\
     0 & -3 & 3 & \vert & 0 \\
     0 & 0 & 0 & \vert & 0
     \end{pmatrix}
     $$
  3. Scale Row 2 by $-\frac{1}{3}$ ($R_2 \leftarrow -\frac{1}{3}R_2$):
     $$
     \begin{pmatrix}
     1 & 2 & -1 & \vert & 0 \\
     0 & 1 & -1 & \vert & 0 \\
     0 & 0 & 0 & \vert & 0
     \end{pmatrix}
     $$

---

### 2. Parametric Form and Free Variables

- **Result:**
  - Free variable: $z = t$ (where $t \in \mathbb{R}$)
  - Parametric solution: $(x, y, z) = (-t, t, t)$

- **Main Steps:**
  1. Translate the reduced row echelon matrix back into equations:
     - Row 2: $y - z = 0 \implies y = z$
     - Row 1: $x + 2y - z = 0$
  2. Since Column 3 lacks a pivot, variable $z$ is a **free variable**. Let $z = t$.
  3. From Row 2, express $y$ in terms of $t$:
     $$
     y = t
     $$
  4. Substitute $y = t$ and $z = t$ into Row 1 to solve for $x$:
     $$
     x + 2(t) - t = 0 \implies x + t = 0 \implies x = -t
     $$

---

### 3. Explanation of Why $(0,0,0)$ Always Satisfies a Homogeneous System

- **Explanation & Reasoning:**
  A homogeneous linear system has zeros on the right-hand side ($Ax = 0$). Substituting the trivial zero vector $x = 0$ into the matrix equation yields:
  $$
  A \cdot 0 = 0
  $$
  Because matrix multiplication by the zero vector always produces a zero vector, every homogeneous system is guaranteed to have at least the trivial solution $(0, 0, 0)$. 
  
  In this specific exercise, because row reduction reveals a free variable ($z = t$), the system has infinitely many non-trivial solutions in addition to the trivial solution, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
