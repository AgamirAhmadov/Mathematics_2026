# Systems of Linear Equations

## Question

### Exercise 2. Gaussian Elimination — One Solution
Solve using Gaussian elimination:

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.


## Solution

Let the augmented matrix $[A \mid b]$ for the given linear system be:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & 1 & \vert & 6 \\
2 & -1 & 1 & \vert & 3 \\
1 & 2 & -1 & \vert & 2
\end{pmatrix}
$$

---

### 1. Set Up and Row Reduction (Forward Elimination)

#### Step 1: Eliminate entries below the pivot in Column 1
Perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
$$
\begin{pmatrix}
1 & 1 & 1 & \vert & 6 \\
0 & -3 & -1 & \vert & -9 \\
0 & 1 & -2 & \vert & -4
\end{pmatrix}
$$

#### Step 2: Swap rows to position a convenient pivot in Column 2
Swap Row 2 ($R_2$) and Row 3 ($R_3$):
$$
R_2 \leftrightarrow R_3
$$
$$
\begin{pmatrix}
1 & 1 & 1 & \vert & 6 \\
0 & 1 & -2 & \vert & -4 \\
0 & -3 & -1 & \vert & -9
\end{pmatrix}
$$

#### Step 3: Eliminate the entry below the pivot in Column 2
Perform $R_3 \leftarrow R_3 + 3R_2$:
$$
\begin{pmatrix}
1 & 1 & 1 & \vert & 6 \\
0 & 1 & -2 & \vert & -4 \\
0 & 0 & -7 & \vert & -21
\end{pmatrix}
$$

---

### 2. Back-Substitution

- **Result:**
  $$
  x = 1, \qquad y = 2, \qquad z = 3
  $$

- **Main Steps:**
  1. **Solve for $z$ from Row 3:**
     $$
     -7z = -21 \implies z = 3
     $$
  2. **Substitute $z$ into Row 2 to solve for $y$:**
     $$
     y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
     $$
  3. **Substitute $y$ and $z$ into Row 1 to solve for $x$:**
     $$
     x + 2 + 3 = 6 \implies x + 5 = 6 \implies x = 1
     $$

---

### 3. Check Consistency (Substitution)

- **Result:**
  - Verified: All three equations are satisfied by $(x, y, z) = (1, 2, 3)$.

- **Main Steps:**
  1. **Equation 1:** $1 + 2 + 3 = 6$ (True)
  2. **Equation 2:** $2(1) - (2) + 3 = 2 - 2 + 3 = 3$ (True)
  3. **Equation 3:** $1 + 2(2) - (3) = 1 + 4 - 3 = 2$ (True)

- **Explanation & Reasoning:**
  Gaussian elimination converts the augmented matrix into row echelon form using elementary row operations. Back-substitution then determines the unique solution, which is verified by direct substitution to ensure complete consistency, formatted in accordance with GitHub Markdown standards and [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
