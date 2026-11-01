# Systems of Linear Equations

## Question

### Exercise 11. A Parameter in a System of Three Equations
Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

> **Why this exercise:** develops parametric analysis while still relying only on elimination.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & 1 & \vert & 1 \\
1 & t & 1 & \vert & 2 \\
1 & 1 & t & \vert & 3
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Step 1: Eliminate entries below the pivot in Column 1**
  Perform $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:
  $$
  \begin{pmatrix}
  1 & 1 & 1 & \vert & 1 \\
  0 & t - 1 & 0 & \vert & 1 \\
  0 & 0 & t - 1 & \vert & 2
  \end{pmatrix}
  $$

---

### 2. Parameter Analysis (Cases Based on $t$)

We examine the pivot coefficients $(t - 1)$ to determine when standard division or elimination steps cease to be valid.

#### Case 1: $t - 1 \neq 0 \implies t \neq 1$ (Unique Solution)
- **Result:** The system has **exactly one unique solution**.
- **Main Steps:**
  1. Since $t \neq 1$, we can divide Row 2 by $(t - 1)$ and Row 3 by $(t - 1)$ (or use back-substitution directly):
     - From Row 2: $(t - 1)y = 1 \implies y = \frac{1}{t - 1}$
     - From Row 3: $(t - 1)z = 2 \implies z = \frac{2}{t - 1}$
  2. Substitute $y$ and $z$ into Row 1 to solve for $x$:
     $$
     x + \frac{1}{t - 1} + \frac{2}{t - 1} = 1 \implies x + \frac{3}{t - 1} = 1 \implies x = 1 - \frac{3}{t - 1} = \frac{t - 4}{t - 1}
     $$
- **Unique Solution Vector:**
  $$
  (x, y, z) = \left(\frac{t - 4}{t - 1}, \frac{1}{t - 1}, \frac{2}{t - 1}\right)
  $$

#### Case 2: $t - 1 = 0 \implies t = 1$ (Inconsistent System)
- **Result:** The system has **no solution** (inconsistent).
- **Main Steps:**
  1. Substitute $t = 1$ back into the reduced augmented matrix:
     $$
     \begin{pmatrix}
     1 & 1 & 1 & \vert & 1 \\
     0 & 0 & 0 & \vert & 1 \\
     0 & 0 & 0 & \vert & 2
     \end{pmatrix}
     $$
  2. Translate Row 2 back into an equation:
     $$
     0x + 0y + 0z = 1 \implies 0 = 1
     $$
  3. Since $0 = 1$ is an impossible mathematical contradiction, the system is inconsistent for $t = 1$.

---

### 3. Summary of Cases

- **$t \neq 1$:** Exactly one unique solution.
- **$t = 1$:** No solution (inconsistent).
- **Infinitely many solutions:** **Never occurs** for any real value of $t$, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
