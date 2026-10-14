### Exercise 8. Row Operations and Their Reversibility
For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

# Exercise 8 Solution

Let the matrix $A$ be defined as follows:

$$
A = \begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3
\end{pmatrix}
$$

---

### 1. Step-by-Step Row Operations

#### Step 1: $R_2 \leftarrow R_2 - 2R_1$
- **Result:**
  $$
  A_1 = \begin{pmatrix}
  1 & 2 & -1 \\
  0 & 0 & 3 \\
  -1 & 1 & 3
  \end{pmatrix}
  $$
- **Main Steps:**
  - Row 1 remains unchanged: $(1, 2, -1)$
  - Subtract $2 \times (\text{Row 1})$ from Row 2: 
    $(2, 4, 1) - 2(1, 2, -1) = (2 - 2, 4 - 4, 1 - (-2)) = (0, 0, 3)$
  - Row 3 remains unchanged: $(-1, 1, 3)$

#### Step 2: $R_3 \leftarrow R_3 + R_1$
- **Result:**
  $$
  A_2 = \begin{pmatrix}
  1 & 2 & -1 \\
  0 & 0 & 3 \\
  0 & 3 & 2
  \end{pmatrix}
  $$
- **Main Steps:**
  - Row 1 remains unchanged: $(1, 2, -1)$
  - Row 2 remains unchanged: $(0, 0, 3)$
  - Add Row 1 to Row 3 (using the current matrix $A_1$): 
    $(-1, 1, 3) + (1, 2, -1) = (-1 + 1, 1 + 2, 3 + (-1)) = (0, 3, 2)$

#### Step 3: Interchange $R_2$ and $R_3$
- **Result:**
  $$
  A_3 = \begin{pmatrix}
  1 & 2 & -1 \\
  0 & 3 & 2 \\
  0 & 0 & 3
  \end{pmatrix}
  $$
- **Main Steps:**
  - Row 1 remains unchanged: $(1, 2, -1)$
  - The old Row 2 becomes the new Row 3: $(0, 0, 3)$
  - The old Row 3 becomes the new Row 2: $(0, 3, 2)$

---

### 2. Reversibility of Operations

Each elementary row operation is reversible, meaning we can always restore the matrix to its previous state by applying the inverse operation:

1. **Reversing Step 1 ($R_2 \leftarrow R_2 - 2R_1$):**
   - **Inverse Operation:** **$R_2 \leftarrow R_2 + 2R_1$**
   - **Explanation:** Since we subtracted twice the first row from the second row, adding twice the first row back cancels out the subtraction and restores the original second row.

2. **Reversing Step 2 ($R_3 \leftarrow R_3 + R_1$):**
   - **Inverse Operation:** **$R_3 \leftarrow R_3 - R_1$**
   - **Explanation:** Since we added the first row to the third row, subtracting the first row from the modified third row reverses the change.

3. **Reversing Step 3 (Interchange $R_2$ and $R_3$):**
   - **Inverse Operation:** **Interchange $R_2$ and $R_3$ again**
   - **Explanation:** Swapping two rows twice sequentially returns them to their original positions.
