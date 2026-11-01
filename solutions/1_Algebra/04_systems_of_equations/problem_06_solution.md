# Systems of Linear Equations

## Question

### Exercise 6. A System with a Parameter — Which Cases Actually Occur?
Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & \vert & 2 \\
a & a & \vert & 4
\end{pmatrix}
$$

---

### 1. Row Reduction and Elimination

- **Main Steps:**
  1. Eliminate the entry below the pivot in Column 1 by performing $R_2 \leftarrow R_2 - aR_1$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     a - a(1) & a - a(1) & \vert & 4 - a(2)
     \end{pmatrix} = \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     0 & 0 & \vert & 4 - 2a
     \end{pmatrix}
     $$

---

### 2. Parameter Analysis (Cases)

Depending on the value of $4 - 2a$, we analyze the possible cases:

#### Case 1: $4 - 2a \neq 0 \implies a \neq 2$ (No Solution)
- **Result:** The system is **inconsistent** (no solution).
- **Explanation:** The second row of the reduced matrix translates to:
  $$
  0x + 0y = 4 - 2a
  $$
  Since $a \neq 2$, the right-hand side is non-zero, yielding an impossible mathematical statement ($0 = \text{non-zero}$). Geometrically, the two equations represent parallel, distinct lines that never intersect.

#### Case 2: $4 - 2a = 0 \implies a = 2$ (Infinitely Many Solutions)
- **Result:** The system has **infinitely many solutions**.
- **Explanation:** Substituting $a = 2$ turns the second row into $0 = 0$. The system reduces to the single independent equation $x + y = 2$. Choosing $y = t$ (where $t \in \mathbb{R}$) yields the parametric solution:
  $$
  (x, y) = (2 - t, t)
  $$
  Geometrically, both equations describe the exact same line, meaning every point on the line is a solution.

#### Case 3: Exactly One Solution
- **Result:** This case **never occurs** for any real value of $a$.
- **Explanation:** The coefficient matrix has identical left-hand side ratios ($1:1$ for $x$ and $y$). The determinant of the coefficient matrix is $1(a) - 1(a) = 0$ for all $a$, meaning the matrix is always singular. Consequently, the lines can never intersect at a single unique point; they are either parallel and disjoint ($a \neq 2$) or identical ($a = 2$).

---

### 3. Summary of Occurring Cases

- **No solution:** Occurs for all $a \neq 2$.
- **Infinitely many solutions:** Occurs when $a = 2$.
- **Exactly one solution:** **Never occurs**, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
