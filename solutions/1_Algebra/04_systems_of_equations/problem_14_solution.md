# Systems of Linear Equations

## Question

### Exercise 14. A Small Change in the Right-Hand Side
Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.


## Solution

---

### 1. Analysis of System 1 ($3x = 3$)

- **Augmented Matrix Setup:**
  $$
  [A \mid b_1] = \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  2 & -1 & \vert & 1 \\
  3 & 0 & \vert & 3
  \end{pmatrix}
  $$

- **Row Reduction:**
  1. Perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     0 & -3 & \vert & -3 \\
     0 & -3 & \vert & -3
     \end{pmatrix}
     $$
  2. Perform $R_3 \leftarrow R_3 - R_2$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     0 & -3 & \vert & -3 \\
     0 & 0 & \vert & 0
     \end{pmatrix}
     $$

- **Solution & Consistency:**
  - From Row 2: $-3y = -3 \implies y = 1$
  - From Row 1: $x + 1 = 2 \implies x = 1$
  - Check in Row 3 ($3x = 3$): $3(1) = 3$ (True).
  - **Result:** System 1 is **consistent** with the unique solution $(x, y) = (1, 1)$.

---

### 2. Analysis of System 2 ($3x = 3.1$)

- **Augmented Matrix Setup:**
  $$
  [A \mid b_2] = \begin{pmatrix}
  1 & 1 & \vert & 2 \\
  2 & -1 & \vert & 1 \\
  3 & 0 & \vert & 3.1
  \end{pmatrix}
  $$

- **Row Reduction:**
  1. Perform $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - 3R_1$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     0 & -3 & \vert & -3 \\
     0 & -3 & \vert & -2.9
     \end{pmatrix}
     $$
  2. Perform $R_3 \leftarrow R_3 - R_2$:
     $$
     \begin{pmatrix}
     1 & 1 & \vert & 2 \\
     0 & -3 & \vert & -3 \\
     0 & 0 & \vert & 0.1
     \end{pmatrix}
     $$

- **Solution & Consistency:**
  - Translate the third row back into an equation:
    $$
    0x + 0y = 0.1 \implies 0 = 0.1
    $$
  - Since $0 = 0.1$ is an impossible mathematical contradiction, no values of $x$ and $y$ can satisfy all three equations simultaneously.
  - **Result:** System 2 is **inconsistent** (no solution).

---

### 3. Explanation: Why a Small Change Alters System Type

- **Explanation & Reasoning:**
  This system is **overdetermined** (it has more equations ($3$) than variables ($2$)). 
  - In an overdetermined system, the first two equations independently determine a unique intersection point $(x, y) = (1, 1)$. 
  - For the entire system to be consistent, this unique intersection point must also satisfy the third equation ($3x = b_3$). 
  - When $b_3 = 3$, the point $(1, 1)$ satisfies the third equation perfectly, making the system consistent. However, when $b_3$ is perturbed even slightly to $3.1$, the third equation demands a coordinate that conflicts with the intersection of the first two lines. 
  - Geometrically, this means the third line fails to pass through the common intersection point of the first two lines, turning a consistent system into an inconsistent one, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
