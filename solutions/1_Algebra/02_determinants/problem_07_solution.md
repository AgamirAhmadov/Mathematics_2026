# Determinants and Invertibility

## Question

### Exercise 7. Using Properties Instead of Recomputing
Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.


## Solution

Let $A$ be a $3 \times 3$ matrix with $\det A = -4$.

---

### 1. Compute $\det(2A)$

- **Result:**
  - $\det(2A) = \mathbf{-32}$

- **Main Steps:**
  1. Identify the dimension $n = 3$ and scalar $c = 2$.
  2. Apply the scaling property formula:
     $$ \det(2A) = 2^3 \cdot \det A = 8 \cdot (-4) = -32 $$

- **Explanation & Property:**
  For any $n \times n$ matrix $A$ and scalar $c$, scaling the entire matrix by $c$ scales each of its $n$ rows by $c$. Therefore:
  $$ \det(cA) = c^n \det A $$

---

### 2. Compute $\det(A^T)$

- **Result:**
  - $\det(A^T) = \mathbf{-4}$

- **Main Steps:**
  1. Apply the transpose determinant identity:
     $$ \det(A^T) = \det A = -4 $$

- **Explanation & Property:**
  Taking the transpose of a matrix swaps its rows and columns, leaving the scalar determinant completely unchanged:
  $$ \det(A^T) = \det A $$

---

### 3. Compute $\det(A^2)$

- **Result:**
  - $\det(A^2) = \mathbf{16}$

- **Main Steps:**
  1. Rewrite $A^2$ as the matrix product $A \cdot A$.
  2. Apply the multiplicative property of determinants:
     $$ \det(A^2) = \det(A \cdot A) = (\det A) \cdot (\det A) = (\det A)^2 $$
  3. Substitute $\det A = -4$:
     $$ \det(A^2) = (-4)^2 = 16 $$

- **Explanation & Property:**
  The determinant of a product of two square matrices equals the product of their individual determinants:
  $$ \det(AB) = \det A \cdot \det B $$

---

### 4. Compute $\det(-A)$

- **Result:**
  - $\det(-A) = \mathbf{4}$

- **Main Steps:**
  1. Recognize $-A$ as scalar multiplication by $c = -1$ for a matrix of size $n = 3$.
  2. Apply the scaling property $\det(cA) = c^n \det A$:
     $$ \det(-A) = (-1)^3 \cdot \det A = (-1) \cdot (-4) = 4 $$

- **Explanation & Property:**
  For an $n \times n$ matrix, $\det(-A) = (-1)^n \det A$. Because the dimension $n = 3$ is odd, $(-1)^3 = -1$, which flips the sign of the original determinant.
