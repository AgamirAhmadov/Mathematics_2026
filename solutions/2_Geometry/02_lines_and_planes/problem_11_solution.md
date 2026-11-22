# Lines and Planes

## Question

### Exercise 11. Plane Containing a Line and a Point
Find the equation of the plane containing

$$
(x,y,z)=(1,0,2)+t(1,1,-1)
$$

and the point $P=(0,2,1)$. Check that both the entire line and the point lie in the plane you obtain.

> **Why this exercise:** requires independently constructing two linearly independent directions in the plane.


## Solution

---

### 1. Construct Two Linearly Independent Direction Vectors in the Plane

From the parametric equation of the line $L : (x, y, z) = (1, 0, 2) + t(1, 1, -1)$:
- A point on the line (at $t = 0$) is $A = (1, 0, 2)$.
- The line's direction vector already lies in the plane:
  $$
  \vec{v}_1 = (1, 1, -1)
  $$

To obtain a second direction vector lying in the plane, form the displacement vector from $A = (1, 0, 2)$ to the given external point $P = (0, 2, 1)$:
$$
\vec{v}_2 = \overrightarrow{AP} = P - A = (0 - 1, \; 2 - 0, \; 1 - 2) = (-1, 2, -1)
$$

Check linear independence: $\vec{v}_1 = (1, 1, -1)$ and $\vec{v}_2 = (-1, 2, -1)$ are not scalar multiples of each other (e.g., the ratio of first components is $-1$, whereas the ratio of second components is $2$), so they span a unique plane.

---

### 2. Compute the Normal Vector Using the Cross Product

A normal vector $\vec{n}$ perpendicular to both $\vec{v}_1$ and $\vec{v}_2$ is given by their cross product:

$$
\vec{n} = \vec{v}_1 \times \vec{v}_2 = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 1 & -1 \\
-1 & 2 & -1
\end{vmatrix}
$$

Expand along the first row:

$$
\vec{n} = \mathbf{i}\big((1)(-1) - (-1)(2)\big) - \mathbf{j}\big((1)(-1) - (-1)(-1)\big) + \mathbf{k}\big((1)(2) - (1)(-1)\big)
$$

$$
\vec{n} = \mathbf{i}(-1 + 2) - \mathbf{j}(-1 - 1) + \mathbf{k}(2 + 1) = (1, 2, 3)
$$

- **Normal Vector:**
  $$
  \vec{n} = (1, 2, 3)
  $$

---

### 3. Equation of the Plane

Using the normal vector $\vec{n} = (1, 2, 3)$ and base point $A = (1, 0, 2)$ in the point-normal equation $A_0(x - x_0) + B_0(y - y_0) + C_0(z - z_0) = 0$:

$$
1(x - 1) + 2(y - 0) + 3(z - 2) = 0
$$

Expand and simplify:

$$
x - 1 + 2y + 3z - 6 = 0 \implies x + 2y + 3z - 7 = 0 \quad \text{(or } x + 2y + 3z = 7\text{)}
$$

- **Result:**
  - General form: $x + 2y + 3z - 7 = 0$

---

### 4. Verification: Point $P$ and the Entire Line Lie in the Plane

- **Check Point $P = (0, 2, 1)$:**
  Substitute $(0, 2, 1)$ into $x + 2y + 3z - 7 = 0$:
  $$
  0 + 2(2) + 3(1) - 7 = 0 + 4 + 3 - 7 = 0 \quad (\text{True})
  $$
  Point $P$ lies on the plane.

- **Check the Entire Line $(x, y, z) = (1 + t, \; t, \; 2 - t)$:**
  Substitute the parametric coordinates of the line into $x + 2y + 3z - 7 = 0$ for an arbitrary parameter $t \in \mathbb{R}$:
  $$
  (1 + t) + 2(t) + 3(2 - t) - 7 = 0
  $$
  Simplify the left-hand side:
  $$
  (1 + 6 - 7) + (t + 2t - 3t) = 0 + 0t = 0 \quad (\text{True for all } t \in \mathbb{R})
  $$
  Because the identity holds for every $t \in \mathbb{R}$, the entire line lies in the plane.

- **Explanation & Reasoning:**
  A plane containing a line and an off-line point is determined by taking the line's direction vector together with a connecting vector from a point on the line to the given point. Taking their cross product yields the normal vector needed to write the plane's equation, and substituting the general parametric coordinates confirms incidence across the whole line rather than at just one point, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
