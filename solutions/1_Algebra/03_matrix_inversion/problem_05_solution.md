## Question

### Exercise 5. A 3×3 Matrix
Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $2\times2$ formula no longer applies.


## Solution

For a $3 \times 3$ matrix, the explicit shortcut formula used for $2 \times 2$ matrices no longer applies, making the Gauss–Jordan elimination method the standard approach. We augment matrix $A$ with the $3 \times 3$ identity matrix $I$ to form the block matrix $[A \mid I]$, then apply elementary row operations until the left side is transformed into $I$, leaving the inverse matrix $A^{-1}$ on the right.

The general row operation rule preserves the solution space of the linear system, satisfying:
$$ [A \mid I] \xrightarrow{\text{Elementary Row Operations}} [I \mid A^{-1}] $$

---

### 1. Set Up the Augmented Matrix $[A \mid I]$

$$
\left[ \begin{array}{ccc|ccc} 
1 & 1 & 0 & 1 & 0 & 0 \\ 
0 & 1 & 1 & 0 & 1 & 0 \\ 
1 & 0 & 1 & 0 & 0 & 1 
\end{array} \right]
$$

---

### 2. Apply Successive Elementary Row Operations

- **Step 1: Eliminate the lower-left entry in column 1.**
  Subtract row 1 from row 3 ($R_3 \leftarrow R_3 - R_1$):
  $$
  \left[ \begin{array}{ccc|ccc} 
  1 & 1 & 0 & 1 & 0 & 0 \\ 
  0 & 1 & 1 & 0 & 1 & 0 \\ 
  0 & -1 & 1 & -1 & 0 & 1 
  \end{array} \right]
  $$

- **Step 2: Eliminate the entry in row 3, column 2.**
  Add row 2 to row 3 ($R_3 \leftarrow R_3 + R_2$):
  $$
  \left[ \begin{array}{ccc|ccc} 
  1 & 1 & 0 & 1 & 0 & 0 \\ 
  0 & 1 & 1 & 0 & 1 & 0 \\ 
  0 & 0 & 2 & -1 & 1 & 1 
  \end{array} \right]
  $$

- **Step 3: Normalize the pivot in row 3.**
  Multiply row 3 by $\frac{1}{2}$ ($R_3 \leftarrow \frac{1}{2}R_3$):
  $$
  \left[ \begin{array}{ccc|ccc} 
  1 & 1 & 0 & 1 & 0 & 0 \\ 
  0 & 1 & 1 & 0 & 1 & 0 \\ 
  0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} 
  \end{array} \right]
  $$

- **Step 4: Clear the entry above the pivot in row 2.**
  Subtract row 3 from row 2 ($R_2 \leftarrow R_2 - R_3$):
  $$
  \left[ \begin{array}{ccc|ccc} 
  1 & 1 & 0 & 1 & 0 & 0 \\ 
  0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\ 
  0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} 
  \end{array} \right]
  $$

- **Step 5: Clear the entry above the pivot in row 1.**
  Subtract row 2 from row 1 ($R_1 \leftarrow R_1 - R_2$):
  $$
  \left[ \begin{array}{ccc|ccc} 
  1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\ 
  0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\ 
  0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} 
  \end{array} \right]
  $$

---

### 3. Resulting Inverse Matrix

Extracting the right-hand block gives the inverse matrix:
$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 
1 & -1 & 1 \\ 
1 & 1 & -1 \\ 
-1 & 1 & 1 
\end{pmatrix}
$$

---

### 4. Verification by Multiplication

To verify our calculation, we check if $A A^{-1} = I$ using the matrix multiplication formula $(AB)_{ij} = \sum_k a_{ik} b_{kj}$:

$$
A A^{-1} = \begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1
\end{pmatrix}
\cdot
\frac{1}{2} \begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix}
$$

Computing the first row product:
- Entry $(1,1)$: $\frac{1}{2}[(1)(1) + (1)(1) + (0)(-1)] = \frac{1}{2}(2) = 1$
- Entry $(1,2)$: $\frac{1}{2}[(1)(-1) + (1)(1) + (0)(1)] = \frac{1}{2}(0) = 0$
- Entry $(1,3)$: $\frac{1}{2}[(1)(1) + (1)(-1) + (0)(1)] = \frac{1}{2}(0) = 0$

Repeating this for all rows yields the identity matrix:
$$
A A^{-1} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I
$$
This confirms that our computed inverse is completely accurate.
