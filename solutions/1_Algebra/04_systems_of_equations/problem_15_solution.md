# Systems of Linear Equations

## Question

### Exercise 15. Classifying Three Systems
For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.


## Solution

---

### 1. System 1 Analysis

- **Augmented Matrix Setup:**
  $$
  [A_1 \mid b_1] = \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  1 & -1 & \vert & 0
  \end{pmatrix}
  $$

- **Elimination:**
  - Perform $R_2 \leftarrow R_2 - R_1$:
    $$
    \begin{pmatrix}
    1 & 1 & \vert & 2 \\
    0 & -2 & \vert & -2
    \end{pmatrix}
    $$

- **Classification & Justification:**
  - **Result:** **Exactly one solution** ($(x, y) = (1, 1)$).
  - **Justification:** The reduced matrix has non-zero pivots in every column corresponding to the variables. There are no rows of zeros or contradiction rows, guaranteeing a unique intersection point.

---

### 2. System 2 Analysis

- **Augmented Matrix Setup:**
  $$
  [A_2 \mid b_2] = \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  2 & 2 & \vert & 4
  \end{pmatrix}
  $$

- **Elimination:**
  - Perform $R_2 \leftarrow R_2 - 2R_1$:
    $$
    \begin{pmatrix}
    1 & 1 & \vert & 2 \\
    0 & 0 & \vert & 0
    \end{pmatrix}
    $$

- **Classification & Justification:**
  - **Result:** **Infinitely many solutions** ($(x, y) = (2 - t, t)$ where $t \in \mathbb{R}$).
  - **Justification:** Elimination yields a complete row of zeros ($0 = 0$) on both sides. The second equation is a scalar multiple of the first, representing the exact same geometric line. This leaves a free variable, generating an infinite family of solutions.

---

### 3. System 3 Analysis

- **Augmented Matrix Setup:**
  $$
  [A_3 \mid b_3] = \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  2 & 2 & \vert & 5
  \end{pmatrix}
  $$

- **Elimination:**
  - Perform $R_2 \leftarrow R_2 - 2R_1$:
    $$
    \begin{pmatrix}
    1 & 1 & \vert & 2 \\
    0 & 0 & \vert & 1
    \end{pmatrix}
    $$

- **Classification & Justification:**
  - **Result:** **No solution (inconsistent)**.
  - **Justification:** Elimination produces a row of zeros on the coefficient side with a non-zero constant on the augmented side, translating to the impossible mathematical statement $0 = 1$. Geometrically, this corresponds to two parallel, distinct lines that never intersect.

- **Summary & Formatting Note:**
  Minimal Gaussian elimination efficiently categorizes linear systems into the three fundamental structural types, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
