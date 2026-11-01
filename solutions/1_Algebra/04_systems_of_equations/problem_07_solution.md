# Systems of Linear Equations

## Question

### Exercise 7. Choosing a Method Deliberately
Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.


## Solution

---

### 1. Triangular Matrix System

- **Chosen Method:** **Back-substitution** (exploiting the upper triangular structure).
- **Execution:**
  1. From the second equation, solve directly for $y$:
     $$
     4y = 8 \implies y = 2
     $$
  2. Substitute $y = 2$ into the first equation to solve for $x$:
     $$
     2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}
     $$
- **Result:** 
  $$
  (x, y) = \left(\frac{5}{2}, 2\right)
  $$
- **Justification:** Because the coefficient matrix is already upper triangular, forward elimination is completely unnecessary. Back-substitution yields the solution in minimal steps.

---

### 2. Three Systems $Ax = b_i$ with a Known Inverse $A^{-1}$

- **Chosen Method:** **Matrix-vector multiplication** ($x_i = A^{-1}b_i$ for each $i = 1, 2, 3$).
- **Plan:** Since the inverse matrix $A^{-1}$ is already known, compute each solution vector directly by multiplying $A^{-1}$ by each respective right-hand side vector $b_1, b_2, b_3$:
  $$
  x_1 = A^{-1}b_1, \qquad x_2 = A^{-1}b_2, \qquad x_3 = A^{-1}b_3
  $$
- **Reusable & Unnecessary Components:**
  - **Reusable:** The pre-computed matrix $A^{-1}$ can be reused across all three right-hand sides.
  - **Unnecessary:** Running Gaussian elimination, LU decomposition, or recomputing row operations from scratch for each separate system is entirely unnecessary.

---

### 3. Single $3 \times 3$ System with an Unknown Inverse

- **Chosen Method:** **Gaussian elimination on the augmented matrix $[A \mid b]$** followed by back-substitution.
- **Plan:** 
  1. Form the augmented matrix $[A \mid b]$.
  2. Apply elementary row operations to reduce the matrix to row echelon form.
  3. Perform back-substitution to find the unique solution vector $x$.
- **Reusable & Unnecessary Components:**
  - **Unnecessary:** Calculating the full inverse matrix $A^{-1}$ is completely unnecessary. Computing an inverse requires $O(n^3)$ operations and yields information for *all* possible right-hand sides, which is inefficient when the goal is restricted to finding a single solution vector for a single right-hand side $b$.

- **Explanation & Reasoning:**
  Choosing a solution method depends strictly on matrix structure (triangular vs. general) and the computational objective (single vs. multiple right-hand sides, or whether an inverse is pre-calculated), formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
