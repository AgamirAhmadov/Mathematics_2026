### Exercise 5. Matrix Times Vector
Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

# Solution

## Exercise 5. Matrix Times Vector

Let the matrix $A$ and vector $x$ be defined as follows:

$$
A = \begin{pmatrix}
2 & -1 \\
1 & 3
\end{pmatrix}, \qquad 
x = \begin{pmatrix}
4 \\
2
\end{pmatrix}
$$

---

### 1. Compute $Ax$

- **Result:** 
  $$
  Ax = \begin{pmatrix}
  6 \\
  10
  \end{pmatrix}
  $$

- **Main Steps:**
  1. Multiply row 1 of $A$ by the vector $x$: $(2)(4) + (-1)(2) = 8 - 2 = 6$
  2. Multiply row 2 of $A$ by the vector $x$: $(1)(4) + (3)(2) = 4 + 6 = 10$

---

### 2. Express $Ax$ as a Linear Combination of the Columns of $A$

- **Result:**
  $$
  Ax = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
  $$

- **Main Steps:**
  1. Identify the columns of matrix $A$: column 1 is $c_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$ and column 2 is $c_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}$.
  2. Extract the entries of vector $x$ to act as scalar coefficients ($x_1 = 4$ and $x_2 = 2$).
  3. Form the linear combination by multiplying each column vector by its corresponding coefficient: $x_1 c_1 + x_2 c_2$.
  4. Perform scalar multiplication followed by vector addition to arrive at the final vector result $\begin{pmatrix} 6 \\ 10 \end{pmatrix}$.

- **Explanation:** 
  Multiplying a matrix by a vector ($Ax$) is fundamentally equivalent to taking a linear combination of the columns of matrix $A$, where the weights (coefficients) are precisely the entries of the vector $x$. This geometric and algebraic perspective bridges individual row-column dot products with column-space transformations.
