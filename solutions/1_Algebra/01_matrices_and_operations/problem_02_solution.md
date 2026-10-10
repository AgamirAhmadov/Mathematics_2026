### Exercise 2. Addition and Scalar Multiplication
For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.



## Solution. Addition and Scalar Multiplication

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
$$

---

### 1. Compute $A+B$

- **Result:** 
  $$
  A + B = \begin{pmatrix}
  5 & 0 \\
  -1 & 8
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Add the corresponding entries of matrices $A$ and $B$ position by position: $(1+4)$, $(2 + (-2))$, $(-1+0)$, $(3+5)$.
  2. Simplify each entry to form the resulting matrix.

- **Explanation:** 
  Matrix addition is performed entry-by-entry. Each element $c_{ij}$ of the sum matrix $C = A + B$ is given by $c_{ij} = a_{ij} + b_{ij}$.

---

### 2. Compute $A-B$

- **Result:** 
  $$
  A - B = \begin{pmatrix}
  -3 & 4 \\
  -1 & -2
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Subtract the corresponding entries of matrix $B$ from matrix $A$: $(1-4)$, $(2 - (-2))$, $(-1-0)$, $(3-5)$.
  2. Simplify each entry to form the resulting matrix.

- **Explanation:** 
  Matrix subtraction is similarly performed entry-by-entry, where each element is computed as $a_{ij} - b_{ij}$.

---

### 3. Compute $3A-2B$

- **Result:** 
  $$
  3A - 2B = \begin{pmatrix}
  -5 & 10 \\
  -3 & -1
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Perform scalar multiplication on $A$ by multiplying every entry by $3$: 
     $$
     3A = \begin{pmatrix} 3 \cdot 1 & 3 \cdot 2 \\ 3 \cdot (-1) & 3 \cdot 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}
     $$
  2. Perform scalar multiplication on $B$ by multiplying every entry by $2$: 
     $$
     2B = \begin{pmatrix} 2 \cdot 4 & 2 \cdot (-2) \\ 2 \cdot 0 & 2 \cdot 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
     $$
  3. Subtract the resulting matrix $2B$ from $3A$: 
     $$
     \begin{pmatrix} 3 - 8 & 6 - (-4) \\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
     $$

- **Explanation:** 
  Scalar multiplication scales every individual entry of a matrix by the given scalar factor. Matrix operations follow standard algebraic precedence where scalar multiplications are computed before addition or subtraction.

---

### 4. Explain why matrix addition is possible only for matrices of the same size.

- **Explanation:** 
  Matrix addition is defined as an entry-by-entry operation. For every element in matrix $A$, there must be a corresponding element in matrix $B$ located at the exact same row and column index ($a_{ij}$ and $b_{ij}$). If the matrices have different dimensions (e.g., a $2 \times 3$ matrix and a $2 \times 2$ matrix), some entries in one matrix would have no corresponding counterpart in the other matrix to add with, making the operation mathematically undefined.
