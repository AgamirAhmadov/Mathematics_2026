# Determinants and Invertibility

## Question

### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.


## Solution

Let $A$ and $B$ be $n \times n$ square matrices with $\det A = 3$ and $\det B = -5$.

---

### 1. Compute $\det(AB)$ and $\det(BA)$

- **Result:**
  - $\det(AB) = \mathbf{-15}$
  - $\det(BA) = \mathbf{-15}$

- **Main Steps:**
  1. Calculate $\det(AB)$ using the multiplicative property:
     $$ \det(AB) = \det A \cdot \det B = (3)(-5) = -15 $$
  2. Calculate $\det(BA)$ using the multiplicative property:
     $$ \det(BA) = \det B \cdot \det A = (-5)(3) = -15 $$

- **Explanation & Formula:**
  For any square matrices $A$ and $B$ of the same dimension, the determinant of a matrix product equals the product of their individual scalar determinants:
  $$ \det(AB) = \det A \cdot \det B $$

---

### 2. Compute $\det(A^{-1}B)$

- **Result:**
  - $\det(A^{-1}B) = \mathbf{-\frac{5}{3}}$

- **Main Steps:**
  1. Verify $A^{-1}$ exists: Since $\det A = 3 \neq 0$, $A$ is invertible, so $A^{-1}$ exists.
  2. Use the inverse determinant property $\det(A^{-1}) = \frac{1}{\det A}$:
     $$ \det(A^{-1}) = \frac{1}{3} $$
  3. Apply the multiplicative property to $\det(A^{-1}B)$:
     $$ \det(A^{-1}B) = \det(A^{-1}) \cdot \det B = \left(\frac{1}{3}\right)(-5) = -\frac{5}{3} $$

- **Explanation & Formula:**
  The determinant of an inverse matrix is the reciprocal of the original matrix's determinant:
  $$ \det(A^{-1}) = (\det A)^{-1} = \frac{1}{\det A} \quad (\text{provided } \det A \neq 0) $$

---

### 3. Explanation of Why $\det(AB) = \det(BA)$ Despite Noncommutativity

- **Explanation & Reasoning:**
  Although matrix multiplication is non-commutative in general (meaning the matrix $AB$ is usually distinct from the matrix $BA$), **scalar multiplication is commutative**.

  When taking the determinant of a product, the operation maps matrix space to real/complex numbers:
  $$ \det(AB) = \det A \cdot \det B $$
  $$ \det(BA) = \det B \cdot \det A $$

  Since $\det A$ and $\det B$ are real numbers (scalars), their scalar product commutes:
  $$ \det A \cdot \det B = \det B \cdot \det A $$

  Therefore, $\det(AB)$ and $\det(BA)$ must always yield the exact same scalar result, even when $AB \neq BA$. Geometrically, both transformations scale $n$-dimensional volume by the same overall factor regardless of the order in which the transformations are composed.
