### Exercise 7. Identity Matrix, Zero Matrix, and Powers
For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

# Solution

## Exercise 7. Identity Matrix, Zero Matrix, and Powers

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
2 & 1 \\
0 & 2
\end{pmatrix}
$$

---

### 1. Computations

#### Compute $AI$
- **Result:**
  $$
  AI = \begin{pmatrix}
  2 & 1 \\
  0 & 2
  \end{pmatrix}
  $$
- **Main Steps:** Multiply $A$ by the $2 \times 2$ identity matrix $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$:
  - Row 1, Col 1: $(2)(1) + (1)(0) = 2$
  - Row 1, Col 2: $(2)(0) + (1)(1) = 1$
  - Row 2, Col 1: $(0)(1) + (2)(0) = 0$
  - Row 2, Col 2: $(0)(0) + (2)(1) = 2$

#### Compute $IA$
- **Result:**
  $$
  IA = \begin{pmatrix}
  2 & 1 \\
  0 & 2
  \end{pmatrix}
  $$
- **Main Steps:** Multiply the identity matrix $I$ by $A$:
  - Row 1, Col 1: $(1)(2) + (0)(0) = 2$
  - Row 1, Col 2: $(1)(1) + (0)(2) = 1$
  - Row 2, Col 1: $(0)(2) + (1)(0) = 0$
  - Row 2, Col 2: $(0)(1) + (1)(2) = 2$

#### Compute $A + 0$
- **Result:**
  $$
  A + 0 = \begin{pmatrix}
  2 & 1 \\
  0 & 2
  \end{pmatrix}
  $$
- **Main Steps:** Add the $2 \times 2$ zero matrix $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$ entry-by-entry to $A$:
  - $(2+0)$, $(1+0)$, $(0+0)$, $(2+0)$

#### Compute $A^2$
- **Result:**
  $$
  A^2 = \begin{pmatrix}
  4 & 4 \\
  0 & 4
  \end{pmatrix}
  $$
- **Main Steps:** Multiply matrix $A$ by itself ($A \cdot A$):
  - Row 1, Col 1: $(2)(2) + (1)(0) = 4$
  - Row 1, Col 2: $(2)(1) + (1)(2) = 4$
  - Row 2, Col 1: $(0)(2) + (2)(0) = 0$
  - Row 2, Col 2: $(0)(1) + (2)(2) = 4$

#### Compute $A^3$
- **Result:**
  $$
  A^3 = \begin{pmatrix}
  8 & 12 \\
  0 & 8
  \end{pmatrix}
  $$
- **Main Steps:** Multiply $A^2$ by $A$:
  - Row 1, Col 1: $(4)(2) + (4)(0) = 8$
  - Row 1, Col 2: $(4)(1) + (4)(2) = 12$
  - Row 2, Col 1: $(0)(2) + (4)(0) = 0$
  - Row 2, Col 2: $(0)(1) + (4)(2) = 8$

---

### 2. Explanations and Observations

#### Roles of Matrices $I$ and $0$
- **Identity Matrix ($I$):** The identity matrix acts as the **multiplicative neutral element** (analogous to the number $1$ in scalar arithmetic). Multiplying any compatible matrix by $I$ on either side leaves the matrix unchanged ($AI = IA = A$).
- **Zero Matrix ($0$):** The zero matrix acts as the **additive neutral element** (analogous to the number $0$ in scalar arithmetic). Adding the zero matrix to any matrix of the same size leaves the matrix unchanged ($A + 0 = A$).

#### Pattern in Successive Powers of $A$
- **Observation:** Looking at the powers computed so far:
  - $A^1 = \begin{pmatrix} 2^1 & 1 \cdot 2^0 \\ 0 & 2^1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$
  - $A^2 = \begin{pmatrix} 2^2 & 2 \cdot 2^1 \\ 0 & 2^2 \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$
  - $A^3 = \begin{pmatrix} 2^3 & 3 \cdot 2^2 \\ 0 & 2^3 \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$
- **General Rule:** For any positive integer $n$, the $n$-th power of matrix $A$ follows the pattern:
  $$
  A^n = \begin{pmatrix}
  2^n & n \cdot 2^{n-1} \\
  0 & 2^n
  \end{pmatrix}
  $$
