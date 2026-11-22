# Lines and Planes

## Question

### Exercise 10. Projection of a Point onto a Plane
Find the orthogonal projection of $P=(2,1,3)$ onto the plane $x+y+z=3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

> **Why this exercise:** combines the normal, intersection, and distance into the construction of a projection and reflection.


## Solution

---

### 1. Construct the Perpendicular Line Through $P$

To project $P = (2, 1, 3)$ orthogonally onto the plane $\Pi : x + y + z = 3$, construct a line $L$ passing through $P$ in the direction of the plane's normal vector:

- **Normal Vector of Plane $\Pi$:**
  From the coefficients of $x + y + z = 3$, read the normal vector:
  $$
  \vec{n} = (1, 1, 1)
  $$

- **Parametric Equations of the Perpendicular Line $L$:**
  Using base point $P = (2, 1, 3)$ and direction vector $\vec{n} = (1, 1, 1)$ with parameter $t \in \mathbb{R}$:
  $$
  \begin{cases}
  x = 2 + t, \\
  y = 1 + t, \\
  z = 3 + t.
  \end{cases}
  $$

---

### 2. Find the Orthogonal Projection $P'$

The orthogonal projection $P'$ is the unique intersection point of the perpendicular line $L$ with the plane $\Pi$. Substitute the parametric coordinates of $L$ into the plane equation $x + y + z = 3$:

$$
(2 + t) + (1 + t) + (3 + t) = 3
$$

Combine like terms and solve for $t$:

$$
6 + 3t = 3 \implies 3t = -3 \implies t = -1
$$

Substitute $t = -1$ back into the parametric equations of $L$ to obtain the coordinates of the projection $P'$:

$$
P' = (2 + (-1), \; 1 + (-1), \; 3 + (-1)) = (1, 0, 2)
$$

- **Result:**
  - The orthogonal projection of $P$ onto the plane is **$P' = (1, 0, 2)$**.

---

### 3. Find the Reflection $P''$ Across the Plane

Because $P'$ is the orthogonal foot on the plane, it lies halfway between the original point $P$ and its mirror reflection $P''$. Moving from $P$ to $P'$ corresponds to a parameter step of $t = -1$ along $\vec{n}$; continuing an equal step further ($t = -2$) reaches $P''$ (equivalently, $P' = \frac{P + P''}{2} \implies P'' = 2P' - P$):

- **Method 1 (Using $t = -2$ along $L$):**
  $$
  P'' = (2 + (-2), \; 1 + (-2), \; 3 + (-2)) = (0, -1, 1)
  $$

- **Method 2 (Midpoint Formula $P'' = 2P' - P$):**
  $$
  P'' = 2(1, 0, 2) - (2, 1, 3) = (2 - 2, \; 0 - 1, \; 4 - 3) = (0, -1, 1)
  $$

- **Result:**
  - The reflection of $P$ across the plane is **$P'' = (0, -1, 1)$**.

---

### 4. Check That the Midpoint Lies on the Plane

Compute the midpoint $M$ of the line segment joining $P = (2, 1, 3)$ and its reflection $P'' = (0, -1, 1)$:

$$
M = \left(\frac{2 + 0}{2}, \; \frac{1 + (-1)}{2}, \; \frac{3 + 1}{2}\right) = \left(\frac{2}{2}, \; \frac{0}{2}, \; \frac{4}{2}\right) = (1, 0, 2)
$$

*(Note that $M$ matches the orthogonal projection $P' = (1, 0, 2)$ exactly.)*

Substitute $M = (1, 0, 2)$ into the plane equation $x + y + z = 3$:

$$
1 + 0 + 2 = 3 \implies 3 = 3 \quad (\text{True})
$$

- **Explanation & Reasoning:**
  Constructing a line parallel to the plane's normal vector guarantees that the shortest perpendicular path from $P$ to the plane is followed. Intersecting this normal line with the plane yields the orthogonal projection $P'$ ($t = -1$), while doubling that displacement ($t = -2$) places the reflection $P''$ symmetrically on the opposite side of the plane, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
