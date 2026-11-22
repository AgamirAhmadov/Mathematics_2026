# Lines and Planes

## Question

### Exercise 4. Plane Through Three Points
Find the equation of the plane through

$$
A=(1,0,0),\quad B=(0,1,0),\quad C=(0,0,1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

> **Why this exercise:** connects earlier vector tools with constructing the equation of a plane.


## Solution

---

### 1. Construct Two Vectors Lying in the Plane

Choose point $A = (1, 0, 0)$ as the initial reference point and form two displacement vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ lying entirely within the plane:

$$
\overrightarrow{AB} = B - A = (0 - 1, 1 - 0, 0 - 0) = (-1, 1, 0)
$$

$$
\overrightarrow{AC} = C - A = (0 - 1, 0 - 0, 1 - 0) = (-1, 0, 1)
$$

---

### 2. Compute the Normal Vector Using the Cross Product

Since both $\overrightarrow{AB}$ and $\overrightarrow{AC}$ lie in the plane, their cross product $\vec{n} = \overrightarrow{AB} \times \overrightarrow{AC}$ is orthogonal to both vectors and therefore serves as a normal vector to the plane:

$$
\vec{n} = \overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
-1 & 1 & 0 \\
-1 & 0 & 1
\end{vmatrix}
$$

Expand the determinant along the first row:

$$
\vec{n} = \mathbf{i}\begin{vmatrix} 1 & 0 \\ 0 & 1 \end{vmatrix} - \mathbf{j}\begin{vmatrix} -1 & 0 \\ -1 & 1 \end{vmatrix} + \mathbf{k}\begin{vmatrix} -1 & 1 \\ -1 & 0 \end{vmatrix}
$$

$$
\vec{n} = \mathbf{i}(1 - 0) - \mathbf{j}(-1 - 0) + \mathbf{k}(0 - (-1)) = (1, 1, 1)
$$

- **Normal Vector:**
  $$
  \vec{n} = (1, 1, 1)
  $$

---

### 3. Equation of the Plane

Using the normal vector $\vec{n} = (1, 1, 1)$ and base point $A = (1, 0, 0)$ in the point-normal formula $A_0(x - x_0) + B_0(y - y_0) + C_0(z - z_0) = 0$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0
$$

$$
x - 1 + y + z = 0 \implies x + y + z - 1 = 0 \quad \text{(or } x + y + z = 1\text{)}
$$

- **Result:**
  - General form: $x + y + z - 1 = 0$

---

### 4. Check the Equation on All Three Points

Substitute the coordinates of $A$, $B$, and $C$ into the plane equation $x + y + z - 1 = 0$:

- **Point $A = (1, 0, 0)$:**
  $$
  1 + 0 + 0 - 1 = 0 \quad (\text{True})
  $$

- **Point $B = (0, 1, 0)$:**
  $$
  0 + 1 + 0 - 1 = 0 \quad (\text{True})
  $$

- **Point $C = (0, 0, 1)$:**
  $$
  0 + 0 + 1 - 1 = 0 \quad (\text{True})
  $$

- **Explanation & Reasoning:**
  Three non-collinear points uniquely determine a plane in $\mathbb{R}^3$. Forming two non-parallel vectors between the points allows us to use the cross product to find a perpendicular normal vector, which directly defines the coefficients of the plane's general equation. Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
