## Question

### Exercise 1. Definition of the Inverse
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.


## Solution

To determine whether matrix $B$ is the inverse of matrix $A$ without using an inverse formula, we apply the fundamental definition of matrix inversion via multiplication: a matrix $B$ is the inverse of $A$ if and only if their product in both orders results in the identity matrix $I$. That is, **$AB = BA = I$**.

The general formula for matrix multiplication of two $2 \times 2$ matrices $X$ and $Y$ to yield entry $(i, j)$ in the product matrix is given by the dot product of row $i$ from the first matrix and column $j$ from the second matrix:
$$ (XY)_{ij} = \sum_{k} x_{ik} y_{kj} $$

---

### 1. Compute $AB$

- **Calculation:**
  $$
  AB = \begin{pmatrix}
  2 & 1 \\
  1 & 1
  \end{pmatrix}
  \begin{pmatrix}
  1 & -1 \\
  -1 & 2
  \end{pmatrix}
  = \begin{pmatrix}
  (2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\
  (1)(1) + (1)(-1) & (1)(-1) + (1)(2)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  AB = \begin{pmatrix}
  2 - 1 & -2 + 2 \\
  1 - 1 & -1 + 2
  \end{pmatrix}
  = \begin{pmatrix}
  1 & 0 \\
  0 & 1
  \end{pmatrix} = I
  $$

- **Explanation & Reasoning:**
  By taking the row-by-column products, each entry is calculated by multiplying corresponding elements and summing them up. The resulting matrix is the $2 \times 2$ identity matrix $I$.

---

### 2. Compute $BA$

- **Calculation:**
  $$
  BA = \begin{pmatrix}
  1 & -1 \\
  -1 & 2
  \end{pmatrix}
  \begin{pmatrix}
  2 & 1 \\
  1 & 1
  \end{pmatrix}
  = \begin{pmatrix}
  (1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\
  (-1)(2) + (2)(1) & (-1)(1) + (2)(1)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  BA = \begin{pmatrix}
  2 - 1 & 1 - 1 \\
  -2 + 2 & -1 + 2
  \end{pmatrix}
  = \begin{pmatrix}
  1 & 0 \\
  0 & 1
  \end{pmatrix} = I
  $$

- **Explanation & Reasoning:**
  Multiplying in the reverse order ($BA$) also yields the identity matrix $I$, confirming symmetry in this relationship.

---

### 3. Conclusion and Relation to the Definition

- **Result:**
  $$ AB = BA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I $$

- **Explanation & Reasoning:**
  By definition, an inverse matrix must satisfy the condition that multiplying it by the original matrix in either order produces the identity matrix. Because both $AB = I$ and $BA = I$, we conclude without using any determinant or adjugate formula that **$B = A^{-1}$**.
