## Question

### Exercise 10. Inverse of a Diagonal Matrix
Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.


## Solution

For diagonal matrices, the determinant is simply the product of the main diagonal entries, and a diagonal matrix is invertible if and only if every entry on its main diagonal is non-zero. 

---

### 1. Determine Invertibility

- **Matrix $D$:**
  The diagonal entries are $2$, $-3$, and $5$. Because none of these entries are zero, the determinant is non-zero ($\det(D) = (2)(-3)(5) = -30 \neq 0$). Therefore, matrix **$D$ is invertible**.

- **Matrix $E$:**
  The diagonal entries are $2$, $0$, and $5$. Because the second diagonal entry is $0$, the determinant is zero ($\det(E) = (2)(0)(5) = 0$). Therefore, matrix **$E$ is not invertible** (it is singular).

---

### 2. Find the Inverse of $D$

- **Formula for a Diagonal Matrix Inverse:**
  For any diagonal matrix $D = \text{diag}(d_1, d_2, \dots, d_n)$ with non-zero diagonal elements, its inverse is obtained by replacing each diagonal entry with its reciprocal:
  $$
  D^{-1} = \text{diag}\left(\frac{1}{d_1}, \frac{1}{d_2}, \dots, \frac{1}{d_n}\right)
  $$

- **Result:**
  Applying this directly to $D$:
  $$
  D^{-1} = \begin{pmatrix}
  \frac{1}{2} & 0 & 0 \\
  0 & -\frac{1}{3} & 0 \\
  0 & 0 & \frac{1}{5}
  \end{pmatrix}
  $$

- **Explanation & Reasoning:**
  Each entry on the diagonal scales space along its respective coordinate axis. To undo this scaling, we must scale by the reciprocal factor along each same axis.

---

### 3. Verification by Multiplication ($DD^{-1}$)

To verify our result, we compute the product $DD^{-1}$:

- **Calculation:**
  $$
  DD^{-1} = \begin{pmatrix}
  2 & 0 & 0 \\
  0 & -3 & 0 \\
  0 & 0 & 5
  \end{pmatrix}
  \begin{pmatrix}
  \frac{1}{2} & 0 & 0 \\
  0 & -\frac{1}{3} & 0 \\
  0 & 0 & \frac{1}{5}
  \end{pmatrix}
  = \begin{pmatrix}
  (2)\left(\frac{1}{2}\right) & 0 & 0 \\
  0 & (-3)\left(-\frac{1}{3}\right) & 0 \\
  0 & 0 & (5)\left(\frac{1}{5}\right)
  \end{pmatrix}
  $$

- **Simplification:**
  $$
  DD^{-1} = \begin{pmatrix}
  1 & 0 & 0 \\
  0 & 1 & 0 \\
  0 & 0 & 1
  \end{pmatrix} = I
  $$

- **Explanation & Reasoning:**
  Multiplying corresponding diagonal elements yields $1$ in every position along the main diagonal, confirming that $DD^{-1} = I$ and verifying our inverse matrix.
