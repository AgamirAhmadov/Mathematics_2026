# Lines and Planes

## Question

### Exercise 8. Intersection Point of a Line and a Plane
Find the intersection point of

$$(x,y,z)=(1,0,2)+t(1,2,-1)$$

with the plane $x+y+z=4$. Check the result by substituting it into both descriptions.

> **Why this exercise:** practices the most important computational case of the line–plane relationship.


## Solution

---

### 1. Parametric Equations of the Line and Plane Normal

From the vector equation of the line $(x, y, z) = (1, 0, 2) + t(1, 2, -1)$, write out the individual coordinate equations in terms of the parameter $t \in \mathbb{R}$:

$$\begin{cases} x = 1 + t, \\ y = 2t, \\ z = 2 - t. \end{cases}$$

*(Note: The direction vector of the line is $\vec{d} = (1, 2, -1)$ and the normal vector of the plane $x + y + z = 4$ is $\vec{n} = (1, 1, 1)$. Since $\vec{d} \cdot \vec{n} = 1(1) + 2(1) + (-1)(1) = 2 \neq 0$, the line is not parallel to the plane and intersects it at a single unique point.)*

---

### 2. Find the Parameter $t$ and Intersection Point

Substitute the parametric expressions for $x$, $y$, and $z$ directly into the plane equation $x + y + z = 4$:

$$(1 + t) + (2t) + (2 - t) = 4$$

Combine like terms and solve for $t$:

$$(1 + 2) + (t + 2t - t) = 4$$

$$3 + 2t = 4 \implies 2t = 1 \implies t = \frac{1}{2}$$

Substitute $t = \frac{1}{2}$ back into the parametric equation of the line to compute the coordinates of the intersection point $P$:

$$P = (1, 0, 2) + \frac{1}{2}(1, 2, -1) = \left(1 + \frac{1}{2}, \; 0 + 1, \; 2 - \frac{1}{2}\right) = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$$

- **Result:**
  - The intersection point is **$P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$**.

---

### 3. Check by Substituting into Both Descriptions

- **Check in the Plane Equation ($x + y + z = 4$):**
  $$\frac{3}{2} + 1 + \frac{3}{2} = \frac{6}{2} + 1 = 3 + 1 = 4 \quad (\text{True})$$
  Thus, $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ satisfies the plane equation.

- **Check in the Line Equation ($(x, y, z) = (1, 0, 2) + t(1, 2, -1)$):**
  Set the parametric representation equal to $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ and solve each coordinate equation independently for the parameter $t$:
  - **x-coordinate:** $1 + t = \frac{3}{2} \implies t = \frac{3}{2} - 1 = \frac{1}{2}$
  - **y-coordinate:** $2t = 1 \implies t = \frac{1}{2}$
  - **z-coordinate:** $2 - t = \frac{3}{2} \implies t = 2 - \frac{3}{2} = \frac{1}{2}$

  Because all three coordinate equations yield the exact same parameter value $t = \frac{1}{2}$, the point $P = \left(\frac{3}{2}, 1, \frac{3}{2}\right)$ also lies on the line.

- **Explanation & Reasoning:**
  Substituting the parametric equations of the line into the implicit equation of the plane reduces the three-dimensional intersection problem to a single linear equation in $t$. Verifying that the resulting point satisfies the plane equation directly and produces a single consistent parameter $t$ across all three line coordinates confirms that $P$ is the unique point common to both geometric objects, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
