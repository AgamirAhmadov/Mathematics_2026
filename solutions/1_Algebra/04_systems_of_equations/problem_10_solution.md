# Systems of Linear Equations

## Question

### Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.


## Solution

Let the general quadratic polynomial be defined as:
$$
p(x) = ax^2 + bx + c
$$

---

### 1. Formulate the System of Equations

Substitute each of the three given points $(x, y)$ into the polynomial equation:
1. For point $(0, 1)$:
   $$
   a(0)^2 + b(0) + c = 1 \implies c = 1
   $$
2. For point $(1, 3)$:
   $$
   a(1)^2 + b(1) + c = 3 \implies a + b + c = 3
   $$
3. For point $(2, 9)$:
   $$
   a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9
   $$

Substitute $c = 1$ into the second and third equations to obtain a $2 \times 2$ linear system in terms of $a$ and $b$:
$$
\begin{cases}
a + b + 1 = 3 \implies a + b = 2 \\
4a + 2b + 1 = 9 \implies 4a + 2b = 8 \implies 2a + b = 4
\end{cases}
$$

---

### 2. Solve the Linear System for Coefficients

Represent the system as an augmented matrix $[A \mid b]$:
$$
[A \mid b] = \begin{pmatrix}
1 & 1 & \vert & 2 \\
2 & 1 & \vert & 4
\end{pmatrix}
$$

#### Row Reduction:
- Perform $R_2 \leftarrow R_2 - 2R_1$:
  $$
  \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  0 & -1 & \vert & 0
  \end{pmatrix}
  $$
- Scale Row 2 ($R_2 \leftarrow -R_2$):
  $$
  \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  0 & 1 & \vert & 0
  \end{pmatrix}
  $$

#### Back-Substitution:
- From Row 2: $b = 0$
- From Row 1: $a + 0 = 2 \implies a = 2$

- **Resulting Coefficients:**
  $$
  a = 2, \qquad b = 0, \qquad c = 1
  $$
  Therefore, the polynomial is:
  $$
  p(x) = 2x^2 + 1
  $$

---

### 3. Check by Substituting All Three Points

- **Point $(0, 1)$:**
  $$
  p(0) = 2(0)^2 + 1 = 1 \quad (\text{True})
  $$
- **Point $(1, 3)$:**
  $$
  p(1) = 2(1)^2 + 1 = 2(1) + 1 = 3 \quad (\text{True})
  $$
- **Point $(2, 9)$:**
  $$
  p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9 \quad (\text{True})
  $$

- **Explanation & Reasoning:**
  Finding unknown polynomial coefficients can be systematically reduced to solving a linear system of equations, where each point imposes a linear condition on the coefficients, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
