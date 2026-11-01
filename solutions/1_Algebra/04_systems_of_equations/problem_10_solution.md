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
