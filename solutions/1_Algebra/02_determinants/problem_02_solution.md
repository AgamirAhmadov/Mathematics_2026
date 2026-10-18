# Determinants and Invertibility

## Question

### Exercise 2. Determinant of a 3×3 Matrix
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.


## Solution

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}
$$

---

### 1. Compute $\det A$ using Sarrus' Rule.

- **Result:**
  - $\det A = \mathbf{41}$

- **Main Steps:**
  1. Write out the matrix and repeat its first two columns to the right:
     $$
     \begin{pmatrix}
     1 & 2 & -1 & \vert & 1 & 2 \\
     0 & 3 & 4 & \vert & 0 & 3 \\
     2 & 1 & 5 & \vert & 2 & 1
     \end{pmatrix}
     $$
  2. Compute the sum of the products along the main diagonals (top-left to bottom-right):
     $$
     \text{Diagonal}_1 = (1)(3)(5) = 15
     $$
     $$
     \text{Diagonal}_2 = (2)(4)(2) = 16
     $$
     $$
     \text{Diagonal}_3 = (-1)(0)(1) = 0
     $$
     $$
     \text{Sum of main diagonals} = 15 + 16 + 0 = 31
     $$
  3. Compute the sum of the products along the anti-diagonals (bottom-left to top-right):
     $$
     \text{Anti-Diagonal}_1 = (2)(3)(-1) = -6
     $$
     $$
     \text{Anti-Diagonal}_2 = (1)(4)(1) = 4
     $$
     $$
     \text{Anti-Diagonal}_3 = (5)(0)(2) = 0
     $$
     $$
     \text{Sum of anti-diagonals} = (-6) + 4 + 0 = -2
     $$
  4. Subtract the sum of anti-diagonals from the sum of main diagonals:
     $$
     \det A = 31 - (-2) = 31 + 2 = 41
     $$

- **Explanation & Formula:**
  Sarrus' rule is a shortcut method strictly applicable to $3 \times 3$ matrices. The general formula evaluates the determinant as:
  $$
  \det A = (a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32}) - (a_{31}a_{22}a_{13} + a_{32}a_{23}a_{11} + a_{33}a_{21}a_{12})
  $$

---

### 2. Perform a check using Laplace Expansion (Cofactor Expansion).

- **Result:**
  - Verified: $\det A = \mathbf{41}$

- **Main Steps:**
  1. Expand along the first column ($C_1$), as it contains a zero entry ($a_{21} = 0$), simplifying the calculation:
     $$
     \det A = a_{11} C_{11} + a_{21} C_{21} + a_{31} C_{31}
     $$
  2. Calculate the non-zero terms:
     $$
     a_{11} C_{11} = 1 \cdot (-1)^{1+1} \det \begin{pmatrix} 3 & 4 \\ 1 & 5 \end{pmatrix} = 1 \cdot (15 - 4) = 11
     $$
     $$
     a_{21} C_{21} = 0
     $$
     $$
     a_{31} C_{31} = 2 \cdot (-1)^{3+1} \det \begin{pmatrix} 2 & -1 \\ 3 & 4 \end{pmatrix} = 2 \cdot (8 - (-3)) = 2 \cdot 15 = 30
     $$
  3. Sum the components:
     $$
     \det A = 11 + 0 + 30 = 41
     $$

- **Explanation & Reasoning:**
  Laplace expansion allows computing the determinant along any row or column. Since expanding along a different line must yield the identical determinant scalar, obtaining $41$ confirms the accuracy of the Sarrus' rule result.
