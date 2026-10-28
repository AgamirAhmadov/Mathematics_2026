## Question

### Exercise 6. Solving a System Using the Inverse
Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.


## Solution

To solve the matrix equation $Ax = b$ using the inverse, we isolate the variable vector $x$ by multiplying both sides from the left by $A^{-1}$:
$$ A^{-1}Ax = A^{-1}b \implies I x = A^{-1}b \implies x = A^{-1}b $$

---

### 1. Find the Inverse Matrix $A^{-1}$

Using the explicit $2 \times 2$ inverse formula $A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$:

- **Determinant Calculation:**
  $$
  \det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
  $$

- **Inverse Matrix:**
  $$
  A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix}
  $$

- **Explanation & Reasoning:**
  Because $\det(A) = 5 \neq 0$, matrix $A$ is invertible. Scaling by $\frac{1}{5}$ distributes across all entries to build the explicit inverse matrix.

---

### 2. Compute the Solution Vector $x = A^{-1}b$

- **Matrix-Vector Multiplication Formula:**
  The vector product $x_i = \sum_j A^{-1}_{ij} b_j$ is computed by taking the dot product of each row of $A^{-1}$ with column vector $b$:
  $$
  x = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix} \begin{pmatrix} 5 \\ 7 \end{pmatrix}
  $$

- **Calculation Steps:**
  - Row 1: $\left(\frac{3}{5}\right)(5) + \left(-\frac{1}{5}\right)(7) = 3 - \frac{7}{5} = \frac{15}{5} - \frac{7}{5} = \frac{8}{5}$
  - Row 2: $\left(-\frac{1}{5}\right)(5) + \left(\frac{2}{5}\right)(7) = -1 + \frac{14}{5} = -\frac{5}{5} + \frac{14}{5} = \frac{9}{5}$

- **Resulting Vector:**
  $$
  x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}
  $$

---

### 3. Verification by Substitution ($Ax = b$)

To check our solution, we substitute vector $x$ back into the original system equation $Ax = b$:

- **Calculation:**
  $$
  Ax = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}
  = \begin{pmatrix} (2)\left(\frac{8}{5}\right) + (1)\left(\frac{9}{5}\right) \\ (1)\left(\frac{8}{5}\right) + (3)\left(\frac{9}{5}\right) \end{pmatrix}
  $$

- **Simplification:**
  $$
  Ax = \begin{pmatrix} \frac{16}{5} + \frac{9}{5} \\ \frac{8}{5} + \frac{27}{5} \end{pmatrix}
  = \begin{pmatrix} \frac{25}{5} \\ \frac{35}{5} \end{pmatrix}
  = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b
  $$

- **Explanation & Reasoning:**
  The matrix multiplication successfully yields the target vector $b$, proving that our solution vector $x = \begin{pmatrix} \frac{8}{5} & \frac{9}{5} \end{pmatrix}^T$ satisfies the system completely.
