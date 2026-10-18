## Exercise 1. Determinant of a 2×2 Matrix
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


### Computations

For a $2 \times 2$ matrix $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is calculated using the formula:

$$
\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc
$$

---

#### 1. Compute $\det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$

- **Result:** **$22$**

- **Main Steps:**
  1. Identify $a = 3$, $b = -2$, $c = 5$, and $d = 4$.
  2. Apply the determinant formula:
     $$
     \det \begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix} = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22
     $$

---

#### 2. Compute $\det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$

- **Result:** **$0$**

- **Main Steps:**
  1. Identify $a = 1$, $b = 7$, $c = 2$, and $d = 14$.
  2. Apply the determinant formula:
     $$
     \det \begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix} = (1)(14) - (7)(2) = 14 - 14 = 0
     $$

---

### Invertibility Analysis

- **Result:** Only the matrix $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$ is **invertible**. The matrix $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$ is **singular (non-invertible)**.

- **Explanation:** 
  A square matrix is invertible if and only if its determinant is non-zero ($\det \neq 0$).
  * For $\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}$, the determinant is $22 \neq 0$, which guarantees that an inverse matrix exists.
  * For $\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}$, the determinant is $0$. Geometrically, the second row is a multiple of the first row ($(2, 14) = 2 \times (1, 7)$), making the rows linearly dependent and causing the matrix to collapse dimensions (zero area/volume), so no inverse exists.
