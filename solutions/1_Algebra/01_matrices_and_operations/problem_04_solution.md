### Exercise 4. Matrix Multiplication and Noncommutativity
For

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
3 & 1 \\
\end{pmatrix}
$$

compute $AB$ and $BA$. Is $AB=BA$? Use this example to explain what noncommutativity of matrix multiplication means.

> **Why this exercise:** shows one of the most important differences between matrix multiplication and multiplication of numbers.

# Solution

## Exercise 4. Matrix Multiplication and Noncommutativity

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 \\
0 & 1
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
2 & 0 \\
3 & 1
\end{pmatrix}
$$

---

### 1. Compute $AB$

- **Result:** 
  $$
  AB = \begin{pmatrix}
  8 & 2 \\
  3 & 1
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Multiply row 1 of $A$ by column 1 of $B$: $(1)(2) + (2)(3) = 2 + 6 = 8$
  2. Multiply row 1 of $A$ by column 2 of $B$: $(1)(0) + (2)(1) = 0 + 2 = 2$
  3. Multiply row 2 of $A$ by column 1 of $B$: $(0)(2) + (1)(3) = 0 + 3 = 3$
  4. Multiply row 2 of $A$ by column 2 of $B$: $(0)(0) + (1)(1) = 0 + 1 = 1$

---

### 2. Compute $BA$

- **Result:** 
  $$
  BA = \begin{pmatrix}
  2 & 4 \\
  3 & 7
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Multiply row 1 of $B$ by column 1 of $A$: $(2)(1) + (0)(0) = 2 + 0 = 2$
  2. Multiply row 1 of $B$ by column 2 of $A$: $(2)(2) + (0)(1) = 4 + 0 = 4$
  3. Multiply row 2 of $B$ by column 1 of $A$: $(3)(1) + (1)(0) = 3 + 0 = 3$
  4. Multiply row 2 of $B$ by column 2 of $A$: $(3)(2) + (1)(1) = 6 + 1 = 7$

---

### 3. Is $AB = BA$?

- **Result:** **No**, $AB \neq BA$.
- **Explanation:** Comparing the resulting matrices, $AB = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}$ and $BA = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}$. Their entries do not match, proving that the order of multiplication alters the outcome.

---

### 4. Explanation of Noncommutativity

- **Explanation:** 
  In ordinary arithmetic with real numbers, multiplication is commutative, meaning that for any two numbers $x$ and $y$, the product $xy$ always equals $yx$ (e.g., $3 \times 5 = 5 \times 3$). 

  Matrix multiplication, however, is **noncommutative**. As demonstrated by this example, changing the order in which matrices are multiplied changes the linear combinations of rows and columns being computed, resulting in entirely different output matrices. In many cases, one product (like $AB$) might even be defined while the reverse product ($BA$) is completely undefined due to dimension incompatibility.
