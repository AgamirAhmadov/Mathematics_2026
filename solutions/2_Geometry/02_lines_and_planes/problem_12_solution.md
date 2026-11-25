# Lines and Planes

## Question

### Exercise 12. Intersection Line of Two Planes
Find a parametric equation of the line that is the intersection of

$$x+y+z=3,\qquad x-y+z=1.$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

> **Why this exercise:** shows the equivalence of the algebraic and geometric approaches to constructing an intersection line.


## Solution

---

### 1. Algebraic Approach: Solve the System of Linear Equations

The points $(x, y, z)$ lying on the intersection line must satisfy both plane equations simultaneously:

$$\begin{cases} x + y + z = 3, \\ x - y + z = 1. \end{cases}$$

Represent the system as an augmented matrix and perform row reduction:

$$\begin{pmatrix} 1 & 1 & 1 & \vert & 3 \\ 1 & -1 & 1 & \vert & 1 \end{pmatrix}$$

1. Perform $R_2 \leftarrow R_2 - R_1$:
   $$\begin{pmatrix} 1 & 1 & 1 & \vert & 3 \\ 0 & -2 & 0 & \vert & -2 \end{pmatrix}$$
2. Scale Row 2 ($R_2 \leftarrow -\frac{1}{2}R_2$):
   $$\begin{pmatrix} 1 & 1 & 1 & \vert & 3 \\ 0 & 1 & 0 & \vert & 1 \end{pmatrix}$$
3. Back-substitute $y = 1$ into Row 1 ($R_1 \leftarrow R_1 - R_2$):
   $$\begin{pmatrix} 1 & 0 & 1 & \vert & 2 \\ 0 & 1 & 0 & \vert & 1 \end{pmatrix}$$

Translate the reduced matrix back into equations:
- $y = 1$
- $x + z = 2 \implies x = 2 - z$

Since Column 3 has no pivot, $z$ is a free variable. Let $z = t$ (where $t \in \mathbb{R}$):

$$\begin{cases} x = 2 - t, \\ y = 1, \\ z = t. \end{cases}$$

In vector parametric form:

$$L : (x, y, z) = (2, 1, 0) + t(-1, 0, 1), \quad t \in \mathbb{R}$$

- **Direction Vector (Method 1 — Algebraic System):**
  $$\vec{d}_1 = (-1, 0, 1)$$

---

### 2. Geometric Approach: Cross Product of the Normal Vectors

The line of intersection lies inside both planes simultaneously, meaning its direction vector must be perpendicular to the normal vectors of both planes:

- Normal vector of Plane 1 ($x + y + z = 3$): $\vec{n}_1 = (1, 1, 1)$
- Normal vector of Plane 2 ($x - y + z = 1$): $\vec{n}_2 = (1, -1, 1)$

Compute the cross product $\vec{d}_2 = \vec{n}_1 \times \vec{n}_2$:

$$\vec{d}_2 = \vec{n}_1 \times \vec{n}_2 = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 1 & 1 & 1 \\ 1 & -1 & 1 \end{vmatrix}$$

Expand along the first row:

$$\vec{d}_2 = \mathbf{i}\big((1)(1) - (1)(-1)\big) - \mathbf{j}\big((1)(1) - (1)(1)\big) + \mathbf{k}\big((1)(-1) - (1)(1)\big)$$

$$\vec{d}_2 = \mathbf{i}(1 + 1) - \mathbf{j}(1 - 1) + \mathbf{k}(-1 - 1) = (2, 0, -2)$$

- **Direction Vector (Method 2 — Cross Product):**
  $$\vec{d}_2 = (2, 0, -2)$$

---

### 3. Comparison of the Results

Compare the two direction vectors obtained from the independent methods:
- From the linear system: $\vec{d}_1 = (-1, 0, 1)$
- From the cross product: $\vec{d}_2 = (2, 0, -2)$

Observe that $\vec{d}_2$ is a non-zero scalar multiple of $\vec{d}_1$:

$$\vec{d}_2 = (2, 0, -2) = -2(-1, 0, 1) = -2\vec{d}_1$$

- **Explanation & Reasoning:**
  Because a direction vector only specifies orientation along a line (and not a fixed length or sense), any non-zero scalar multiple defines the exact same geometric line. The algebraic elimination method naturally normalizes the free parameter $z = t$ to coefficient $1$ (yielding $\vec{d}_1 = (-1, 0, 1)$), while the geometric cross product produces a parallel vector scaled by $-2$ ($\vec{d}_2 = (2, 0, -2)$). Both confirm that the intersection line runs parallel to the $xz$-plane at constant height $y = 1$, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
