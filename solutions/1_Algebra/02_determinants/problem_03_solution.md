# Determinants and Invertibility

## Question

### Exercise 3. Swapping Two Rows
For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.


## Solution

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1
\end{pmatrix}
$$

---

### 1. Compute $\det A$.

- **Result:**
  - $\det A = \mathbf{5}$

- **Main Steps:**
  1. Expand along the first row ($R_1$) using Laplace expansion:
     $$
     \det A = 1 \cdot \det \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} - 2 \cdot \det \begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} + 0 \cdot \det \begin{pmatrix} 0 & 3 \\ 2 & 1 \end{pmatrix}
     $$
  2. Compute the $2 \times 2$ determinants:
     $$
     \det \begin{pmatrix} 3 & 1 \\ 1 & 1 \end{pmatrix} = (3)(1) - (1)(1) = 3 - 1 = 2
     $$
     $$
     \det \begin{pmatrix} 0 & 1 \\ 2 & 1 \end{pmatrix} = (0)(1) - (1)(2) = 0 - 2 = -2
     $$
  3. Combine the terms:
     $$
     \det A = 1(2) - 2(-2) + 0 = 2 + 4 = 5
     $$

- **Explanation & Formula:**
  Laplace expansion breaks down a $3 \times 3$ determinant into weighted $2 \times 2$ sub-determinants along any row or column:
  $$
  \det A = \sum_{j=1}^{n} (-1)^{i+j} a_{ij} M_{ij}
  $$

---

### 2. Form Matrix $B$ and Predict $\det B$.

- **Result:**
  - Matrix $B = \begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}$
  - Prediction: $\det B = \mathbf{-5}$

- **Explanation & Property:**
  A fundamental property of determinants states that **interchanging any two rows (or columns) of a matrix reverses the sign of its determinant**:
  $$
  \det(B) = -\det(A)
  $$
  Since matrix $B$ is obtained by swapping $R_1$ and $R_2$ of matrix $A$, and $\det A = 5$, the predicted value of $\det B$ is $-5$.

---

### 3. Verify $\det B$ by Direct Calculation.

- **Result:**
  - Verified: $\det B = \mathbf{-5}$

- **Main Steps:**
  1. Write matrix $B$:
     $$
     B = \begin{pmatrix}
     0 & 3 & 1 \\
     1 & 2 & 0 \\
     2 & 1 & 1
     \end{pmatrix}
     $$
  2. Expand along the first row ($R_1$) of $B$:
     $$
     \det B = 0 \cdot \det \begin{pmatrix} 2 & 0 \\ 1 & 1 \end{pmatrix} - 3 \cdot \det \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} + 1 \cdot \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix}
     $$
  3. Compute the $2 \times 2$ sub-determinants:
     $$
     \det \begin{pmatrix} 1 & 0 \\ 2 & 1 \end{pmatrix} = (1)(1) - (0)(2) = 1
     $$
     $$
     \det \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} = (1)(1) - (2)(2) = 1 - 4 = -3
     $$
  4. Combine the terms:
     $$
     \det B = 0 - 3(1) + 1(-3) = -3 - 3 = -6 \quad \text{Wait, let's re-verify: }
     $$
     Let's re-evaluate Sarrus' rule for $B$:
     - Main diagonals: $(0)(2)(1) + (3)(0)(2) + (1)(1)(1) = 0 + 0 + 1 = 1$
     - Anti-diagonals: $(2)(2)(1) + (1)(0)(0) + (1)(1)(3) = 4 + 0 + 3 = 7$
     - $\det B = 1 - 7 = -6$? Let's double check $A$:
       - $A$ main diagonals: $(1)(3)(1) + (2)(1)(2) + (0)(0)(1) = 3 + 4 + 0 = 7$
       - $A$ anti-diagonals: $(2)(3)(0) + (1)(1)(1) + (1)(0)(2) = 0 + 1 + 0 = 1$
       - $\det A = 7 - 1 = 6$
  
  *Correction of Step 1:*
  1. Main diagonals of $A$: $(1 \cdot 3 \cdot 1) + (2 \cdot 1 \cdot 2) + (0 \cdot 0 \cdot 1) = 3 + 4 + 0 = 7$
  2. Anti-diagonals of $A$: $(2 \cdot 3 \cdot 0) + (1 \cdot 1 \cdot 1) + (1 \cdot 0 \cdot 2) = 0 + 1 + 0 = 1$
  3. $\det A = 7 - 1 = 6$
  
  4. Recalculate prediction: $\det B = -6$
  5. Recalculate calculation for $B$:
     $$
     \det B = 0 - 3(1) + 1(-3) = -3 - 3 = -6
     $$

- **Final Corrected Summary:**
  - $\det A = \mathbf{6}$
  - Predicted $\det B = -\det A = \mathbf{-6}$
  - Calculated $\det B = \mathbf{-6}$
  - The row-swap determinant property is fully confirmed.
