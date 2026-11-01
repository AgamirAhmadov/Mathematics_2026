# Systems of Linear Equations

## Question

### Exercise 9. A System from a Sum Condition
Find numbers $x,y$ satisfying

$$
x+y=10,\qquad 2x+5y=32.
$$

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

### Exercise 10. A Polynomial Through Three Points
Find a polynomial $p(x)=ax^2+bx+c$ whose graph passes through $(0,1)$, $(1,3)$, and $(2,9)$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.


## Solution

---

### Exercise 9. A System from a Sum Condition

#### 1. Set Up and Augmented Matrix
Let the system be represented as an augmented matrix:
$$
[A \mid b] = \begin{pmatrix}
1 & 1 & \vert & 10 \\
2 & 5 & \vert & 32
\end{pmatrix}
$$

#### 2. Row Reduction
- Perform $R_2 \leftarrow R_2 - 2R_1$:
  $$
  \begin{pmatrix}
  1 & 1 & \vert & 10 \\
  0 & 3 & \vert & 12
  \end{pmatrix}
  $$
- Scale Row 2 ($R_2 \leftarrow \frac{1}{3}R_2$):
  $$
  \begin{pmatrix}
  1 & 1 & \vert & 10 \\
  0 & 1 & \vert & 4
  \end{pmatrix}
  $$

#### 3. Back-Substitution & Solution
- From Row 2: $y = 4$
- From Row 1: $x + 4 = 10 \implies x = 6$
- **Result:** $(x, y) = (6, 4)$

#### 4. Geometric Explanation of Uniqueness
- **Explanation:** The two equations represent linear functions (lines) in the 2D Cartesian plane with distinct slopes ($m_1 = -1$ and $m_2 = -\frac{2}{5}$). Because their slopes are unequal, the lines are neither parallel nor coincident; they intersect at exactly one unique coordinate point $(6, 4)$, which corresponds to the single unique solution of the system.

---

### Exercise 10. A Polynomial Through Three Points

#### 1. Formulate the System of Equations
Given the general quadratic polynomial $p(x) = ax^2 + bx + c$, substitute each of the three given points $(0,1)$, $(1,3)$, and $(2,9)$ into the equation:
- For $(0,1)$: 
  $$ a(0)^2 + b(0) + c = 1 \implies c = 1 $$
- For $(1,3)$: 
  $$ a(1)^2 + b(1) + c = 3 \implies a + b + c = 3 $$
- For $(2,9)$: 
  $$ a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9 $$

Substitute $c = 1$ into the second and third equations to obtain a $2 \times 2$ linear system in terms of $a$ and $b$:
$$
\begin{cases}
a + b + 1 = 3 \implies a + b = 2 \\
4a + 2b + 1 = 9 \implies 4a + 2b = 8 \implies 2a + b = 4
\end{cases}
$$

#### 2. Solve the Linear System for Coefficients
Represent the reduced system as an augmented matrix:
$$
\begin{pmatrix}
1 & 1 & \vert & 2 \\
2 & 1 & \vert & 4
\end{pmatrix}
$$
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
- **Back-Substitution:**
  - $b = 0$
  - $a + 0 = 2 \implies a = 2$

- **Resulting Polynomial:**
  $$
  p(x) = 2x^2 + 0x + 1 \implies p(x) = 2x^2 + 1
  $$

#### 3. Check by Substitution
- Point $(0,1)$: $p(0) = 2(0)^2 + 1 = 1$ (True)
- Point $(1,3)$: $p(1) = 2(1)^2 + 1 = 2(1) + 1 = 3$ (True)
- Point $(2,9)$: $p(2) = 2(2)^2 + 1 = 2(4) + 1 = 9$ (True)

Formatted in accordance with GitHub Markdown standards in conjunction with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
