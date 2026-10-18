# Determinants and Invertibility

## Question

### Exercise 5. Row Operations
For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.


## Solution

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}
$$

---

### 1. Step-by-Step Row Reduction and Determinant Tracking

#### Step 1: Eliminate entries below the pivot in Column 1
Perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 + R_1$:

$$
A_1 = \begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5
\end{pmatrix}
$$

- **Determinant Change:** **No change.** 
- **Property:** Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + c R_j$) leaves the determinant unchanged ($\det A_1 = \det A$).

---

#### Step 2: Factor out a scalar from Row 2
Factor out $-3$ from $R_2$:

$$
A_2 = \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 6 & 5
\end{pmatrix}
$$

- **Determinant Change:** **Multiplied by $-3$.**
- **Property:** Multiplying a single row by a scalar $c$ scales the entire determinant by $c$. Therefore:
  $$ \det A_1 = -3 \cdot \det A_2 \implies \det A = -3 \cdot \det A_2 $$

---

#### Step 3: Eliminate entry below the pivot in Column 2
Perform $R_3 \leftarrow R_3 - 6R_2$:

$$
A_3 = \begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & -7
\end{pmatrix}
$$

- **Determinant Change:** **No change.**
- **Property:** Adding a scalar multiple of one row to another row does not change the determinant ($\det A_3 = \det A_2$).

---

### 2. Compute $\det A$ from Upper Triangular Form

- **Result:**
  - $\det A = \mathbf{21}$

- **Main Steps:**
  1. Matrix $A_3$ is now in upper triangular form. The determinant of an upper triangular matrix is the product of its main diagonal entries:
     $$ \det A_3 = (1) \cdot (1) \cdot (-7) = -7 $$
  2. Substitute $\det A_3$ back into the relationship established in Step 2 ($\det A = -3 \cdot \det A_3$):
     $$ \det A = -3 \cdot (-7) = 21 $$

- **Explanation & Formula:**
  By applying Gaussian elimination, any square matrix can be transformed into an upper triangular matrix $U$. By tracking how each elementary row operation affects the determinant (swaps change sign by $-1$, row scaling factors out $c$, and row additions leave the determinant invariant), we can compute $\det A$ efficiently as:
  $$ \det A = c_1 \cdot c_2 \cdots c_k \cdot \prod_{i=1}^{n} u_{ii} $$
