# Systems of Linear Equations

## Question

### Exercise 4. Infinitely Many Solutions
Solve

$$
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & 1 & \vert & 2 \\
2 & 2 & 2 & \vert & 4 \\
1 & -1 & 1 & \vert & 0
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Main Steps:**
  1. Eliminate entries below the pivot in Column 1: perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
     $$
     \begin{pmatrix}
     1 & 1 & 1 & \vert & 2 \\
     0 & 0 & 0 & \vert & 0 \\
     0 & -2 & 0 & \vert & -2
     \end{pmatrix}
     $$
  2. Swap $R_2$ and $R_3$ to place the non-zero row in row echelon form ($R_2 \leftrightarrow R_3$):
     $$
     \begin{pmatrix}
     1 & 1 & 1 & \vert & 2 \\
     0 & -2 & 0 & \vert & -2 \\
     0 & 0 & 0 & \vert & 0
     \end{pmatrix}
     $$
  3. Scale Row 2 by $-\frac{1}{2}$ ($R_2 \leftarrow -\frac{1}{2}R_2$):
     $$
     \begin{pmatrix}
     1 & 1 & 1 & \vert & 2 \\
     0 & 1 & 0 & \vert & 1 \\
     0 & 0 & 0 & \vert & 0
     \end{pmatrix}
     $$

---

### 2. Parametric Form and Identification of Free Variables

- **Result:**
  - Free variable: $z = t$ (where $t \in \mathbb{R}$)
  - Parametric solution: $(x, y, z) = (1 - t, 1, t)$

- **Main Steps:**
  1. Translate the reduced row echelon matrix back into equations:
     - Row 2: $y = 1$
     - Row 1: $x + y + z = 2$
  2. Since there is no pivot in the column for $z$, variable $z$ is a **free variable**. Let $z = t$.
  3. Substitute $y = 1$ and $z = t$ into Row 1 to solve for $x$:
     $$
     x + 1 + t = 2 \implies x = 1 - t
     $$

---

### 3. Check for a Chosen Parameter Value

- **Result:**
  - Let $t = 2$. The resulting point is $(x, y, z) = (-1, 1, 2)$.
  - **Verification:**
    - Equation 1: $(-1) + (1) + (2) = 2$ (True)
    - Equation 2: $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (True)
    - Equation 3: $(-1) - (1) + (2) = -2 + 2 = 0$ (True)

- **Explanation & Reasoning:**
  When Gaussian elimination results in a row of zeros equal to zero (`[0 0 0 | 0]`), it indicates linear dependence and fewer pivot variables than unknowns. The variables lacking pivots become free parameters, generating an infinite family of solutions (a line or plane in space), formatted in accordance with GitHub Markdown standards and [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
