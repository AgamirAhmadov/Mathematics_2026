# Systems of Linear Equations

## Question

### Exercise 5. Row Echelon Form and Number of Solutions
For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.


## Solution

Let the given augmented matrix be in row echelon form:

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0
\end{pmatrix}
$$

---

### 1. Determine the Number of Solutions

- **Result:**
  - The system has **infinitely many solutions**.

- **Main Steps:**
  1. Inspect the augmented matrix for consistency: there is no row of the form $(0 \quad 0 \quad 0 \mid c)$ where $c \neq 0$, meaning the system is **consistent**.
  2. Compare the number of pivot variables with the total number of variables:
     - Total number of variables ($n$): $3$ ($x, y, z$).
     - Number of non-zero rows (pivots): $2$.
  3. Since the number of pivots ($2$) is less than the number of variables ($3$), and the system is consistent, there are infinitely many solutions.

---

### 2. Parametric Form and Free Variables

- **Result:**
  - Free variable: $z = t$ (where $t \in \mathbb{R}$)
  - Parametric solution: $(x, y, z) = (1 + 5t, 1 - 2t, t)$

- **Main Steps:**
  1. Translate the row echelon matrix back into equations:
     - Row 2: $y + 2z = 1 \implies y = 1 - 2z$
     - Row 1: $x + 2y - z = 3$
  2. Identify free variables: Columns 1 and 2 contain pivots ($x$ and $y$ are pivot variables). Column 3 lacks a pivot, so $z$ is a **free variable**. Let $z = t$.
  3. Express $y$ in terms of $t$:
     $$
     y = 1 - 2t
     $$
  4. Substitute $y$ and $z$ into the first equation to solve for $x$:
     $$
     x + 2(1 - 2t) - t = 3
     $$
     $$
     x + 2 - 4t - t = 3 \implies x + 2 - 5t = 3 \implies x = 1 + 5t
     $$

---

### 3. Explanation of Free Variables

- **Explanation & Reasoning:**
  The number of variables that can be chosen freely is determined by the formula:
  $$
  \text{Number of free variables} = (\text{Total variables } n) - (\text{Number of pivot columns } r)
  $$
  In this matrix, $n = 3$ and $r = 2$, yielding $3 - 2 = 1$ free variable. Each free variable introduces one independent real parameter ($t$), generating a 1-dimensional line of infinite solutions, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
