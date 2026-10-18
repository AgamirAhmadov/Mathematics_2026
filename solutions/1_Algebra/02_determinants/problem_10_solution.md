# Determinants and Invertibility

## Question

### Exercise 10. Detecting Dependence
Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.


## Solution

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5
\end{pmatrix}
$$

---

### 1. Identify Row Dependence

- **Result:**
  - Row 2 is an exact scalar multiple of Row 1: $R_2 = 2R_1$.

- **Main Steps:**
  1. Examine the first row: $R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}$.
  2. Examine the second row: $R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}$.
  3. Factor out $2$ from the second row: 
     $$
     R_2 = 2 \cdot \begin{pmatrix} 1 & 2 & 3 \end{pmatrix} = 2R_1
     $$

---

### 2. Explanation of $\det A = 0$ Without Full Calculation

- **Result:**
  - $\det A = \mathbf{0}$

- **Explanation & Property:**
  A fundamental property of determinants states that **if a square matrix has two rows (or columns) that are scalar multiples of each other (linearly dependent), its determinant is automatically zero**:
  $$
  \det A = 0
  $$
  Because $R_2 = 2R_1$, the rows of $A$ are linearly dependent. Geometrically, this means the vectors defining the matrix's rows lie in a shared lower-dimensional subspace, enclosing zero volume in 3D space and forcing the determinant to vanish.

---

### 3. Connection to Noninvertibility

- **Result:**
  - Matrix $A$ is **singular (non-invertible)**.

- **Explanation & Reasoning:**
  A square matrix is invertible if and only if its determinant is non-zero ($\det A \neq 0$). 
  
  Since $\det A = 0$, matrix $A$ collapses 3D space onto a flat plane or line (dimensional collapse), destroying information about unique vector origins. Consequently, no inverse matrix $A^{-1}$ can exist to undo the transformation.
