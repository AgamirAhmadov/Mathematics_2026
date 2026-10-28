## Question

### Exercise 4. Gauss–Jordan
Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.


## Solution

The Gauss–Jordan method for finding an inverse relies on augmenting the target matrix $A$ with an identity matrix of the same dimensions, forming the block matrix $[A \mid I]$. By applying elementary row operations, we transform the left side into the identity matrix $I$. Through this process, the same sequence of operations automatically converts the right side into the inverse matrix $A^{-1}$.

---

### 1. Set Up the Augmented Matrix $[A \mid I]$

We begin by placing matrix $A$ on the left and the $2 \times 2$ identity matrix $I$ on the right:

$$
\left[ \begin{array}{cc|cc} 
1 & 2 & 1 & 0 \\ 
3 & 5 & 0 & 1 
\end{array} \right]
$$

---

### 2. Apply Successive Elementary Row Operations

- **Step 1: Eliminate the entry below the first pivot.**
  We want a $0$ in the position of the $3$ (row 2, column 1). We subtract $3$ times row 1 from row 2 ($R_2 \leftarrow R_2 - 3R_1$):
  $$
  \left[ \begin{array}{cc|cc} 
  1 & 2 & 1 & 0 \\ 
  3 - 3(1) & 5 - 3(2) & 0 - 3(1) & 1 - 3(0) 
  \end{array} \right]
  =
  \left[ \begin{array}{cc|cc} 
  1 & 2 & 1 & 0 \\ 
  0 & -1 & -3 & 1 
  \end{array} \right]
  $$

- **Step 2: Scale the second row to make the pivot equal to $1$.**
  Multiply row 2 by $-1$ ($R_2 \leftarrow -R_2$):
  $$
  \left[ \begin{array}{cc|cc} 
  1 & 2 & 1 & 0 \\ 
  0 & 1 & 3 & -1 
  \end{array} \right]
  $$

- **Step 3: Eliminate the entry above the second pivot.**
  We want a $0$ in the position of the $2$ (row 1, column 2). We subtract $2$ times row 2 from row 1 ($R_1 \leftarrow R_1 - 2R_2$):
  $$
  \left[ \begin{array}{cc|cc} 
  1 - 2(0) & 2 - 2(1) & 1 - 2(3) & 0 - 2(-1) \\ 
  0 & 1 & 3 & -1 
  \end{array} \right]
  =
  \left[ \begin{array}{cc|cc} 
  1 & 0 & -5 & 2 \\ 
  0 & 1 & 3 & -1 
  \end{array} \right]
  $$

---

### 3. Result and Explanation of Why It Works

- **Result:**
  $$
  A^{-1} = \begin{pmatrix} 
  -5 & 2 \\ 
  3 & -1 
  \end{pmatrix}
  $$

- **Explanation & Reasoning:**
  Each elementary row operation can be represented as multiplication by an elementary matrix $E_i$. Transforming matrix $A$ into the identity matrix $I$ means applying a product of elementary matrices such that:
  $$ (E_k \cdots E_2 E_1) A = I $$
  By definition, if a matrix multiplied by another yields the identity matrix, that product represents the inverse:
  $$ (E_k \cdots E_2 E_1) = A^{-1} $$
  Because we applied the exact same sequence of row operations to the identity matrix on the right side:
  $$ (E_k \cdots E_2 E_1) I = A^{-1} I = A^{-1} $$
  This mathematical equivalence guarantees that whatever appears on the right side once the left side becomes $I$ is precisely the inverse matrix $A^{-1}$.
