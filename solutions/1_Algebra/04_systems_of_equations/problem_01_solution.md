# Systems of Linear Equations

## Question

### Exercise 1. From a System to a Matrix
Write the system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

in the form $Ax=b$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.


## Solution

Let the given system of linear equations be represented in matrix form as $Ax = b$.

---

### 1. Identify the Matrix Components ($A$, $x$, and $b$)

- **Result:**
  - Coefficient Matrix $A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}$
  - Vector of Unknowns $x = \begin{pmatrix} x \\ y \\ z \end{pmatrix}$
  - Right-Hand Side Vector $b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}$

- **Main Steps:**
  1. Extract the coefficients of the variables $x$, $y$, and $z$ from each equation to form the rows of matrix $A$:
     - Equation 1 ($2x - y + z = 4$): coefficients are $2$, $-1$, $1$.
     - Equation 2 ($x + 3y - 2z = 1$): coefficients are $1$, $3$, $-2$.
     - Equation 3 ($3x + y + z = 7$): coefficients are $3$, $1$, $1$.
  2. List the variables in order as a column vector $x$.
  3. Extract the constant terms from the right-hand side of each equation as the vector $b$.

---

### 2. Matrix Equation Form ($Ax = b$)

- **Result:**
  $$
  \begin{pmatrix}
  2 & -1 & 1 \\
  1 & 3 & -2 \\
  3 & 1 & 1
  \end{pmatrix} \begin{pmatrix}
  x \\
  y \\
  z
  \end{pmatrix} = \begin{pmatrix}
  4 \\
  1 \\
  7
  \end{pmatrix}
  $$

---

### 3. Explanation of Row-to-Equation Correspondence

- **Explanation & Reasoning:**
  Each row of the matrix equation corresponds directly to one linear equation through matrix-vector multiplication (the dot product of a row vector with the vector of unknowns):
  - **Row 1:** $(2)(x) + (-1)(y) + (1)(z) = 2x - y + z = 4$, matching the first equation.
  - **Row 2:** $(1)(x) + (3)(y) + (-2)(z) = x + 3y - 2z = 1$, matching the second equation.
  - **Row 3:** $(3)(x) + (1)(y) + (1)(z) = 3x + y + z = 7$, matching the third equation.
  
  Formatted in accordance with GitHub Markdown standards in conjunction with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
