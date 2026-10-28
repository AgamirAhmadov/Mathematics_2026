## Question

### Exercise 9. Matrix Equation
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.


## Solution

### 1. Determining the Side for $A^{-1}$

- **Decision:** 
  We must multiply by $A^{-1}$ from the **left** on both sides of the equation.

- **Explanation & Reasoning:**
  Matrix multiplication is not commutative (i.e., $AX \neq XA$). Because matrix $A$ multiplies $X$ from the left in the expression $AX = B$, we must preserve this order when applying the inverse to isolate $X$:
  $$
  AX = B \implies A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies X = A^{-1}B
  $$
  If we had multiplied from the right ($XA = B$), it would yield a completely different algebraic expression.

---

### 2. Find the Inverse Matrix $A^{-1}$

- **Determinant Calculation:**
  For $A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, the determinant is:
  $$
  \det(A) = (1)(1) - (2)(0) = 1 - 0 = 1
  $$

- **Applying the $2 \times 2$ Inverse Formula:**
  $$
  A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix} = \frac{1}{1} \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}
  $$

---

### 3. Compute $X = A^{-1}B$

- **Matrix Multiplication Setup:**
  $$
  X = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}
  $$

- **Calculation Steps:**
  $$
  X = \begin{pmatrix}
  (1)(3) + (-2)(2) & (1)(1) + (-2)(4) \\
  (0)(3) + (1)(2) & (0)(1) + (1)(4)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  X = \begin{pmatrix}
  3 - 4 & 1 - 8 \\
  0 + 2 & 0 + 4
  \end{pmatrix}
  = \begin{pmatrix}
  -1 & -7 \\
  2 & 4
  \end{pmatrix}
  $$

---

### 4. Verification by Computing $AX$

To check our solution, we substitute $X$ back into the original equation and compute $AX$:

- **Calculation:**
  $$
  AX = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}
  $$
  $$
  AX = \begin{pmatrix}
  (1)(-1) + (2)(2) & (1)(-7) + (2)(4) \\
  (0)(-1) + (1)(2) & (0)(-7) + (1)(4)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  AX = \begin{pmatrix}
  -1 + 4 & -7 + 8 \\
  0 + 2 & 0 + 4
  \end{pmatrix}
  = \begin{pmatrix}
  3 & 1 \\
  2 & 4
  \end{pmatrix} = B
  $$

- **Explanation & Reasoning:**
  Because $AX$ successfully returns matrix $B$, our calculated solution matrix $X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}$ is verified to be correct.
