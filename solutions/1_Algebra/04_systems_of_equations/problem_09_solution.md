# Systems of Linear Equations

## Question

### Exercise 9. A System from a Sum Condition
Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.


## Solution

Let the given system of linear equations be represented as an augmented matrix $[A \mid b]$:

$$
[A \mid b] = \begin{pmatrix}
1 & 1 & \vert & 10 \\
2 & 5 & \vert & 32
\end{pmatrix}
$$

---

### 1. Row Reduction (Forward Elimination)

- **Main Steps:**
  1. Eliminate the entry below the pivot in Column 1 by performing $R_2 \leftarrow R_2 - 2R_1$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 10 \\
     2 - 2(1) & 5 - 2(1) & \vert & 32 - 2(10)
     \end{pmatrix} = \begin{pmatrix}
     1 & 1 & \vert & 10 \\
     0 & 3 & \vert & 12
     \end{pmatrix}
     $$
  2. Scale Row 2 to obtain a leading $1$ ($R_2 \leftarrow \frac{1}{3}R_2$):
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 10 \\
     0 & 1 & \vert & 4
     \end{pmatrix}
     $$

---

### 2. Back-Substitution and Solution

- **Result:**
  $$
  x = 6, \qquad y = 4
  $$

- **Main Steps:**
  1. **Solve for $y$ from Row 2:**
     $$
     y = 4
     $$
  2. **Substitute $y$ into Row 1 to solve for $x$:**
     $$
     x + 4 = 10 \implies x = 6
     $$

---

### 3. Geometric Explanation of Uniqueness

- **Explanation & Reasoning:**
  Each linear equation represents a straight line in the 2D Cartesian coordinate plane:
  - Line 1 ($x + y = 10$ has slope $m_1 = -1$)
  - Line 2 ($2x + 5y = 32$ has slope $m_2 = -\frac{2}{5}$)

  Because their slopes are distinct ($m_1 \neq m_2$), the two lines are neither parallel nor coincident. Consequently, they intersect at exactly one unique coordinate point $(6, 4)$, which corresponds to the unique solution of the linear system, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
