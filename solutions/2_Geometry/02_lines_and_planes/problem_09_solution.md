# Lines and Planes

## Question

### Exercise 9. Distances
Compute:

1. the distance from $P=(2,3)$ to the line $3x+4y-10=0$,
2. the distance from $Q=(2,-1,3)$ to the plane $2x-2y+z-4=0$.

Compare the two formulas and explain their common connection with the normal direction.

> **Why this exercise:** organizes two similar formulas through one geometric idea.


## Solution

---

### 1. Distance from Point $P=(2,3)$ to the Line $3x+4y-10=0$

The perpendicular distance $d$ from a point $P = (x_0, y_0)$ to a line in general form $Ax + By + C = 0$ is given by:

$$d = \frac{\vert{}Ax_0 + By_0 + C\vert{}}{\sqrt{A^2 + B^2}}$$

Identify the coefficients and coordinates:
- Line coefficients: $A = 3$, $B = 4$, $C = -10$ (normal vector $\vec{n} = (3, 4)$)
- Point coordinates: $x_0 = 2$, $y_0 = 3$

Substitute the values into the formula:

$$d = \frac{\vert{}3(2) + 4(3) - 10\vert{}}{\sqrt{3^2 + 4^2}} = \frac{\vert{}6 + 12 - 10\vert{}}{\sqrt{9 + 16}} = \frac{\vert{}8\vert{}}{\sqrt{25}} = \frac{8}{5} = 1.6$$

- **Result:**
  - The distance from $P=(2,3)$ to the line is **$\frac{8}{5}$** (or **$1.6$**).

---

### 2. Distance from Point $Q=(2,-1,3)$ to the Plane $2x-2y+z-4=0$

The perpendicular distance $D$ from a point $Q = (x_0, y_0, z_0)$ to a plane in general form $Ax + By + Cz + D_0 = 0$ is given by:

$$D = \frac{\vert{}Ax_0 + By_0 + Cz_0 + D_0\vert{}}{\sqrt{A^2 + B^2 + C^2}}$$

Identify the coefficients and coordinates:
- Plane coefficients: $A = 2$, $B = -2$, $C = 1$, $D_0 = -4$ (normal vector $\vec{n} = (2, -2, 1)$)
- Point coordinates: $x_0 = 2$, $y_0 = -1$, $z_0 = 3$

Substitute the values into the formula:

$$D = \frac{\vert{}2(2) - 2(-1) + 1(3) - 4\vert{}}{\sqrt{2^2 + (-2)^2 + 1^2}} = \frac{\vert{}4 + 2 + 3 - 4\vert{}}{\sqrt{4 + 4 + 1}} = \frac{\vert{}5\vert{}}{\sqrt{9}} = \frac{5}{3}$$

- **Result:**
  - The distance from $Q=(2,-1,3)$ to the plane is **$\frac{5}{3}$**.

---

### 3. Comparison of the Two Formulas and Geometric Connection

- **Structural Comparison:**
  Both formulas share the exact same algebraic structure:
  $$\text{Distance} = \frac{\vert{}\text{Implicit equation evaluated at the external point}\vert{}}{\|\vec{n}\|}$$
  In $\mathbb{R}^2$, the normal vector to the line has two components $\vec{n} = (A, B)$ with Euclidean norm $\|\vec{n}\| = \sqrt{A^2 + B^2}$. In $\mathbb{R}^3$, the normal vector to the plane extends naturally to three components $\vec{n} = (A, B, C)$ with norm $\|\vec{n}\| = \sqrt{A^2 + B^2 + C^2}$.

- **Common Connection with the Normal Direction (Orthogonal Projection):**
  The shortest distance from an external point $X_0$ to a line (in 2D) or a plane (in 3D) is measured strictly along the **normal direction** $\vec{n}$, which is perpendicular to the geometric object.
  
  If $X_1$ is any point lying on the line or plane, the vector $\overrightarrow{X_1 X_0}$ connects that reference point to the external point. Projecting $\overrightarrow{X_1 X_0}$ onto the unit normal vector $\hat{n} = \frac{\vec{n}}{\|\vec{n}\|}$ isolates the perpendicular component of that displacement:
  $$\text{Distance} = \left\vert{} \overrightarrow{X_1 X_0} \cdot \hat{n} \right\vert{} = \frac{\vert{}\vec{n} \cdot \overrightarrow{X_1 X_0}\vert{}}{\|\vec{n}\|}$$
  Because $X_1$ lies on the line or plane, it satisfies $\vec{n} \cdot X_1 + C = 0$ (or $\vec{n} \cdot X_1 + D_0 = 0$), which simplifies the numerator directly to $\vert{}\vec{n} \cdot X_0 + C\vert{}$. Thus, both formulas express the exact same geometric principle: **scalar orthogonal projection onto the unit normal vector**, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
