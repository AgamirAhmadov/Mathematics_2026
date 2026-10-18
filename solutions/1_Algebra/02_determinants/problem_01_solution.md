# Determinants and Invertibility

## Question

### Exercise 1. Determinant of a 2×2 Matrix
Compute

$$
\det
\begin{pmatrix}
3 & -2 \\
5 & 4 \\
\end{pmatrix},\qquad \det
\begin{pmatrix}
1 & 7 \\
2 & 14 \\
\end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.


## Solution

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
3 & -2 \\
5 & 4
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
1 & 7 \\
2 & 14
\end{pmatrix}
$$

---

### 1. Compute $\det A$ and $\det B$.

- **Result:**
  - $\det A = \mathbf{22}$
  - $\det B = \mathbf{0}$

- **Main Steps:**
  1. Calculate $\det A$:
     $$ \det A = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22 $$
  2. Calculate $\det B$:
     $$ \det B = (1)(14) - (7)(2) = 14 - 14 = 0 $$

- **Explanation & Formula:**
  For any $2 \times 2$ matrix, the determinant is computed using the standard formula:
  $$ \det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc $$
  This formula measures the scaling factor of the transformation formed by the matrix, taking the product of the main diagonal ($ad$) and subtracting the product of the anti-diagonal ($bc$).

---

### 2. Which matrix is invertible? Justify your answer.

- **Result:**
  - Matrix $A$ is **invertible**.
  - Matrix $B$ is **singular (non-invertible)**.

- **Main Steps:**
  1. Check the non-zero condition for $\det A$: $22 \neq 0 \implies A^{-1} \text{ exists}$.
  2. Check the zero condition for $\det B$: $\det B = 0 \implies B^{-1} \text{ does not exist}$.

- **Explanation & Reasoning:**
  A square matrix is invertible if and only if its determinant is non-zero:
  $$ A \text{ is invertible} \iff \det(A) \neq 0 $$
  - **Matrix $A$:** Since $\det A = 22 \neq 0$, matrix $A$ preserves dimensionality and can be inverted.
  - **Matrix $B$:** Since $\det B = 0$, the matrix causes a dimensional collapse (its second row $(2, 14)$ is a scalar multiple of its first row $(1, 7)$). Because the rows are linearly dependent, the transformation maps space onto a line with zero area, making it impossible to invert back to the original space.
