# Lines and Planes

## Question

### Exercise 7. A Line Relative to a Plane
For

$$L:(x,y,z)=(1,1,0)+t(1,-1,0),\qquad \Pi:x+y+z=2,$$

determine whether the line intersects the plane at one point, is parallel to it, or lies in it. Explain the role of the dot product of the direction vector and the normal vector.

> **Why this exercise:** builds a universal test for the relative position of a line and a plane.


## Solution

---

### 1. Extract Geometric Components

From the given equations, identify the base point and direction vector of the line $L$, as well as the normal vector of the plane $\Pi$:

- **Line $L$:**
  - Base point ($t = 0$): $P_0 = (1, 1, 0)$
  - Direction vector: $\vec{d} = (1, -1, 0)$
  - Parametric coordinates:
    $$\begin{cases} x = 1 + t, \\ y = 1 - t, \\ z = 0. \end{cases}$$

- **Plane $\Pi$ ($x + y + z = 2$):**
  - Normal vector: $\vec{n} = (1, 1, 1)$

---

### 2. Test for Parallelism via the Dot Product

Compute the dot product $\vec{d} \cdot \vec{n}$ between the direction vector of the line and the normal vector of the plane:

$$\vec{d} \cdot \vec{n} = (1)(1) + (-1)(1) + (0)(1) = 1 - 1 + 0 = 0$$

- **Interpretation:**
  Since $\vec{d} \cdot \vec{n} = 0$, the direction vector $\vec{d}$ is orthogonal (perpendicular) to the plane's normal vector $\vec{n}$. Consequently, the line $L$ runs parallel to the plane $\Pi$ (it either is strictly parallel with zero intersection points, or lies entirely inside the plane).

---

### 3. Determine Whether the Line Lies in the Plane or Is Strictly Parallel

To distinguish between the two parallel cases, substitute the parametric coordinates of $L$ into the equation of $\Pi$ (or test whether the base point $P_0 = (1, 1, 0)$ satisfies $\Pi$):

$$(1 + t) + (1 - t) + 0 = 2$$

Simplify the left-hand side:

$$2 + 0t = 2 \implies 2 = 2$$

- **Result:**
  Because the equation $2 = 2$ holds identically for **all** values of the parameter $t \in \mathbb{R}$, every point on $L$ satisfies the equation of $\Pi$. Therefore, **the line $L$ lies entirely in the plane $\Pi$**.

---

### 4. Role of the Dot Product $\vec{d} \cdot \vec{n}$

- **Explanation & Reasoning:**
  In three-dimensional space ($\mathbb{R}^3$), the dot product $\vec{d} \cdot \vec{n}$ serves as a universal algebraic test for the relative orientation of a line and a plane:
  1. **If $\vec{d} \cdot \vec{n} \neq 0$:** The direction vector is not perpendicular to the normal vector, meaning the line tilts toward the plane and **intersects it at a single unique point**.
  2. **If $\vec{d} \cdot \vec{n} = 0$:** The direction vector is perpendicular to the normal vector, meaning the line maintains a constant distance from the plane and is parallel to its surface. Substituting a single point from the line into the plane equation then separates
