# Determinants and Invertibility

## Question

### Exercise 4. Triangular Matrix
Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.


## Solution

Let the upper triangular matrix $T$ be defined as follows:

$$
T = \begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7
\end{pmatrix}
$$

---

### 1. Compute $\det T$.

- **Result:**
  - $\det T = \mathbf{-42}$

- **Main Steps:**
  1. Identify the entries along the main diagonal: $t_{11} = 2$, $t_{22} = -3$, and $t_{33} = 7$.
  2. Multiply these diagonal entries together:
     $$
     \det T = (2) \times (-3) \times (7) = -6 \times 7 = -42
     $$

---

### 2. State the Rule for an Arbitrary Triangular Matrix.

- **Rule:**
  The determinant of any upper triangular, lower triangular, or diagonal matrix is equal to the product of its main diagonal entries:
  $$
  \det T = \prod_{i=1}^{n} t_{ii} = t_{11} \cdot t_{22} \cdots t_{nn}
  $$

---

### 3. Explanation using the Example.

- **Explanation & Reasoning:**
  We can understand why this rule holds by observing what happens if we perform Laplace (cofactor) expansion sequentially along the first column:

  1. **Expand along Column 1:** Since all entries below the first element ($t_{11} = 2$) are zero, expanding along the first column collapses the determinant to a single non-zero term:
     $$
     \det T = 2 \cdot \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix}
     $$
  2. **Expand the $2 \times 2$ sub-determinant:** The resulting sub-matrix is itself lower-left zeroed. Applying the $2 \times 2$ determinant formula ($ad - bc$):
     $$
     \det \begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = (-3)(7) - (5)(0) = (-3)(7)
     $$
  3. **Combine terms:** Putting it together gives $\det T = 2 \cdot (-3) \cdot 7 = -42$.

  Because all off-diagonal entries in the lower triangle are zero, every anti-diagonal or off-diagonal product term in the full determinant expansion evaluates to zero, leaving only the product of the main diagonal elements.
