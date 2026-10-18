# Determinants and Invertibility

## Question

### Exercise 9. Area and the Determinant
The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.


## Solution

Let the vectors $u$ and $v$ be defined as follows:

$$
u = \begin{pmatrix} 3 \\ 1 \end{pmatrix}, \qquad 
v = \begin{pmatrix} 1 \\ 4 \end{pmatrix}
$$

---

### 1. Compute the Area using a Determinant

- **Result:**
  - $\text{Area} = \mathbf{11}$

- **Main Steps:**
  1. Form a $2 \times 2$ matrix $M = (u \quad v)$ using the vectors as columns:
     $$
     M = \begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}
     $$
  2. Compute the determinant of $M$:
     $$
     \det M = (3)(4) - (1)(1) = 12 - 1 = 11
     $$
  3. Take the absolute value to find the geometric area:
     $$
     \text{Area} = |\det M| = |11| = 11
     $$

- **Explanation & Formula:**
  In 2D space, the area of a parallelogram spanned by two column vectors $u$ and $v$ is given by the absolute value of the determinant of the matrix formed by those vectors:
  $$
  \text{Area} = \left| \det \begin{pmatrix} u & v \end{pmatrix} \right|
  $$

---

### 2. Reverse the Order of the Vectors

- **Result:**
  - Reversed Matrix $M' = \begin{pmatrix} v & u \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}$
  - $\det M' = \mathbf{-11}$
  - $\text{Area} = \mathbf{11}$

- **Main Steps:**
  1. Compute the determinant of the reversed matrix $M'$:
     $$
     \det M' = (1)(1) - (3)(4) = 1 - 12 = -11
     $$
  2. Compute the area by taking the absolute value:
     $$
     \text{Area} = |\det M'| = |-11| = 11
     $$

---

### 3. Geometric Explanation: Determinant Sign vs. Area

- **What Changes in the Determinant:**
  - The **sign** of the determinant changes from $+11$ to $-11$.
  - Reversing the order of vectors is equivalent to swapping the two columns of the matrix, which reverses the sign of the determinant:
    $$
    \det \begin{pmatrix} v & u \end{pmatrix} = -\det \begin{pmatrix} u & v \end{pmatrix}
    $$
  - The sign represents the **orientation** (or handiness) of the ordered vector pair. In $(u, v)$, turning from $u$ to $v$ follows a counterclockwise path (positive orientation). In $(v, u)$, turning from $v$ to $u$ follows a clockwise path (negative orientation).

- **What Does Not Change in the Area:**
  - The **magnitude** (absolute value) of the determinant remains exactly $11$, so the physical area of the parallelogram is completely unchanged.
  - Geometrically, swapping the roles of the two spanning vectors reflects the orientation of the shape but leaves its physical size and surface area invariant:
    $$
    \text{Area} = |\det M| = |-11| = 11
    $$
