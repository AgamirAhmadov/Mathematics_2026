### Exercise 10. Columns of a Matrix Product
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a full product of two matrices instead of simply repeating another $Ax$ exercise.

# Exercise 10 Solution

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1
\end{pmatrix}
$$

Let the columns of $B$ be denoted by $b_1$ and $b_2$:
$$
b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \qquad 
b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}
$$

---

### 1. Compute $Ab_1$ and $Ab_2$

#### Compute $Ab_1$
- **Result:**
  $$
  Ab_1 = \begin{pmatrix}
  -1 \\
  2
  \end{pmatrix}
  $$
- **Main Steps:** Multiply matrix $A$ by the column vector $b_1$:
  - Row 1: $(1)(1) + (2)(-1) + (0)(3) = 1 - 2 + 0 = -1$
  - Row 2: $(0)(1) + (1)(-1) + (1)(3) = 0 - 1 + 3 = 2$

#### Compute $Ab_2$
- **Result:**
  $$
  Ab_2 = \begin{pmatrix}
  2 \\
  1
  \end{pmatrix}
  $$
- **Main Steps:** Multiply matrix $A$ by the column vector $b_2$:
  - Row 1: $(1)(2) + (2)(0) + (0)(1) = 2 + 0 + 0 = 2$
  - Row 2: $(0)(2) + (1)(0) + (1)(1) = 0 + 0 + 1 = 1$

---

### 2. Compute the Matrix $AB$

- **Result:**
  $$
  AB = \begin{pmatrix}
  -1 & 2 \\
  2 & 1
  \end{pmatrix}
  $$
- **Main Steps:** Multiply the $2 \times 3$ matrix $A$ by the $3 \times 2$ matrix $B$:
  - Row 1, Col 1: $(1)(1) + (2)(-1) + (0)(3) = -1$
  - Row 1, Col 2: $(1)(2) + (2)(0) + (0)(1) = 2$
  - Row 2, Col 1: $(0)(1) + (1)(-1) + (1)(3) = 2$
  - Row 2, Col 2: $(0)(2) + (1)(0) + (1)(1) = 1$

---

### 3. Comparison and Explanation

- **Comparison:** 
  Comparing the columns of the product matrix $AB$ with the vectors computed in Part 1:
  - Column 1 of $AB$ is $\begin{pmatrix} -1 \\ 2 \end{pmatrix}$, which matches $Ab_1$.
  - Column 2 of $AB$ is $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$, which matches $Ab_2$.

- **Explanation:** 
  Matrix multiplication can be understood from a column-oriented perspective. When you compute a product $AB$, each column of the resulting matrix is formed by multiplying matrix $A$ by the corresponding individual column vector of $B$. Therefore, the $j$-th column of $AB$ is always equal to $Ab_j$. This approach reveals that matrix multiplication is essentially a batch collection of multiple matrix-vector products performed simultaneously.
