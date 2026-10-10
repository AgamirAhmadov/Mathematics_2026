### Exercise 6. Transpose
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

# Solution

## Transpose

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3
\end{pmatrix}
$$

---

### 1. Compute $A^T$, $B^T$, and $AB$

#### Compute $A^T$
- **Result:**
  $$
  A^T = \begin{pmatrix}
  1 & 4 \\
  2 & 5 \\
  3 & 6
  \end{pmatrix}
  $$
- **Explanation:** The transpose of a matrix is formed by swapping its rows and columns. Since $A$ is a $2 \times 3$ matrix, its transpose $A^T$ is a $3 \times 2$ matrix where entry $(i, j)$ of $A^T$ comes from entry $(j, i)$ of $A$.

#### Compute $B^T$
- **Result:**
  $$
  B^T = \begin{pmatrix}
  1 & 2 & -1 \\
  0 & 1 & 3
  \end{pmatrix}
  $$
- **Explanation:** Similarly, the $3 \times 2$ matrix $B$ is transposed into a $2 \times 3$ matrix $B^T$ by swapping its rows and columns.

#### Compute $AB$
- **Result:**
  $$
  AB = \begin{pmatrix}
  2 & 11 \\
  8 & 23
  \end{pmatrix}
  $$
- **Main Steps:**
  - Row 1, Col 1: $(1)(1) + (2)(2) + (3)(-1) = 1 + 4 - 3 = 2$
  - Row 1, Col 2: $(1)(0) + (2)(1) + (3)(3) = 0 + 2 + 9 = 11$
  - Row 2, Col 1: $(4)(1) + (5)(2) + (6)(-1) = 4 + 10 - 6 = 8$
  - Row 2, Col 2: $(4)(0) + (5)(1) + (6)(3) = 0 + 5 + 18 = 23$

---

### 2. Verify $(AB)^T = B^T A^T$

#### Compute Left-Hand Side: $(AB)^T$
- **Result:**
  $$
  (AB)^T = \begin{pmatrix}
  2 & 8 \\
  11 & 23
  \end{pmatrix}
  $$
- **Steps:** Take the matrix product $AB$ computed above and transpose it by swapping its rows and columns.

#### Compute Right-Hand Side: $B^T A^T$
- **Result:**
  $$
  B^T A^T = \begin{pmatrix}
  2 & 8 \\
  11 & 23
  \end{pmatrix}
  $$
- **Steps:** Multiply the $2 \times 3$ matrix $B^T$ by the $3 \times 2$ matrix $A^T$:
  - Row 1, Col 1: $(1)(1) + (2)(2) + (-1)(3) = 1 + 4 - 3 = 2$
  - Row 1, Col 2: $(1)(4) + (2)(5) + (-1)(6) = 4 + 10 - 6 = 8$
  - Row 2, Col 1: $(0)(1) + (1)(2) + (3)(3) = 0 + 2 + 9 = 11$
  - Row 2, Col 2: $(0)(4) + (1)(5) + (3)(6) = 0 + 5 + 18 = 23$

#### Verification Conclusion
- **Result:** Since $(AB)^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$ and $B^T A^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, we have successfully verified that **$(AB)^T = B^T A^T$**.

- **Explanation:** 
  The transpose of a product of two matrices reverses the order of multiplication: the transpose of $AB$ is equal to the product of their transposes in reverse order ($B^T A^T$). This is an essential identity in linear algebra.
