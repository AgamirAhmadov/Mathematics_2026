# Analytic Geometry in the Plane and Space

## Question

### Exercise 3. Plane Through a Point with a Given Normal Vector
Find the equation of the plane through $P=(1,-2,3)$ and perpendicular to $n=(2,1,-1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

> **Why this exercise:** shows the basic construction of a plane from a point and a normal vector.


## Solution

---

### 1. Equation of the Plane

A plane passing through a known point $P = (x_0, y_0, z_0)$ with a normal vector $\vec{n} = (A, B, C)$ is defined by the dot product condition $\vec{n} \cdot \overrightarrow{PX} = 0$, where $X = (x, y, z)$ is any point on the plane:

$$
A(x - x_0) + B(y - y_0) + C(z - z_0) = 0
$$

Substitute $P = (1, -2, 3)$ and $\vec{n} = (2, 1, -1)$ into the equation:

$$
2(x - 1) + 1(y - (-2)) - 1(z - 3) = 0
$$

Expand and simplify:

$$
2x - 2 + y + 2 - z + 3 = 0
$$

$$
2x + y - z + 3 = 0 \quad \text{(or } 2x + y - z = -3\text{)}
$$

- **Result:**
  - General form: $2x + y - z + 3 = 0$

---

### 2. Verification by Substituting Point $P$

Substitute the coordinates of $P = (1, -2, 3)$ back into the derived plane equation $2x + y - z + 3 = 0$:

$$
2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0 \quad (\text{True})
$$

- **Result:**
  - Verified: Point $P = (1, -2, 3)$ lies on the plane.

---

### 3. Role of the Normal Vector

- **Explanation & Reasoning:**
  In three-dimensional space ($\mathbb{R}^3$), the **normal vector** $\vec{n} = (2, 1, -1)$ uniquely determines the **orientation (tilt)** of the plane by being strictly perpendicular (orthogonal) to every vector lying inside the plane. 
  
  For any arbitrary point $X = (x, y, z)$ on the plane, the displacement vector $\overrightarrow{PX} = (x - 1, y + 2, z - 3)$ lies entirely within the plane, requiring its dot product with $\vec{n}$ to equal zero ($\vec{n} \cdot \overrightarrow{PX} = 0$). Once the orientation is fixed by $\vec{n}$, passing through a single point $P$ pins down the exact position of the plane in space.

  Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
