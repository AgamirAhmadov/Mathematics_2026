## Question

### Exercise 3. When Does the Inverse Not Exist?
For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.


## Solution

A square matrix is non-invertible (singular) and lacks an inverse if it fails to span the full space, meaning it collapses dimensions. We can prove why matrix $A$ has no inverse using two distinct perspectives: the determinant formula and row dependence.

---

### 1. Proof Using the Determinant

- **Formula:**
  For a general $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse formula is:
  $$
  A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}
  $$
  The term $ad - bc$ is the **determinant** ($\det(A)$). If $\det(A) = 0$, the formula requires division by zero, which is undefined.

- **Calculation:**
  Here, $a = 2$, $b = 4$, $c = 1$, and $d = 2$:
  $$
  \det(A) = (2)(2) - (4)(1) = 4 - 4 = 0
  $$

- **Explanation & Reasoning:**
  Because the determinant evaluates to $0$, the scalar multiplier $\frac{1}{\det(A)}$ becomes $\frac{1}{0}$, rendering the explicit inverse formula invalid. A zero determinant indicates that the matrix scales space down to a lower dimension (collapsing a 2D plane onto a 1D line), destroying the information needed to reverse the transformation.

---

### 2. Proof Using Linear Dependence Between Rows

- **Observation:**
  Let the rows of matrix $A$ be denoted as row vectors:
  - Row 1: $R_1 = \begin{pmatrix} 2 & 4 \end{pmatrix}$
  - Row 2: $R_2 = \begin{pmatrix} 1 & 2 \end{pmatrix}$

- **Relationship:**
  Notice that the first row is a scalar multiple of the second row:
  $$
  R_1 = 2 R_2 \quad \text{or} \quad R_2 = \frac{1}{2} R_1
  $$

- **Explanation & Reasoning:**
  When the rows (or columns) of a square matrix are scalar multiples of each other, they are **linearly dependent**. In linear algebra, an invertible matrix requires its rows to be linearly independent so they form a full-basis that spans the entire space. 

  Since $R_1$ and $R_2$ point in the exact same directional ratio, the matrix maps a 2D input space onto a 1D line, losing directional information. Because this transformation is irreversible (many input vectors map to the same output), no inverse matrix $A^{-1}$ can exist.
