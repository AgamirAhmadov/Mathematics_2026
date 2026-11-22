# Analytic Geometry in the Plane and Space

## Question

### Exercise 1. Line Through Two Points
Find the equation of the line through $A=(1,2)$ and $B=(4,-1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

> **Why this exercise:** teaches how to move between equivalent descriptions of a line and connect them with the appropriate vectors.


## Solution

---

### 1. Direction Vector and Parametric Form

- **Direction Vector:**
  Compute the vector $\vec{d} = \overrightarrow{AB}$ from point $A=(1,2)$ to point $B=(4,-1)$:
  $$
  \vec{d} = B - A = (4 - 1, -1 - 2) = (3, -3)
  $$
  *(Note: Any non-zero scalar multiple, such as $\vec{d}_0 = (1, -1)$, is also a valid direction vector.)*

- **Parametric Form:**
  Using base point $A=(1,2)$ and direction vector $\vec{d}=(3,-3)$ with parameter $t \in \mathbb{R}$:
  $$
  \begin{cases}
  x = 1 + 3t, \\
  y = 2 - 3t.
  \end{cases}
  $$
  *(Or equivalently, using $\vec{d}_0 = (1, -1)$: $x = 1 + t$, $y = 2 - t$.)*

---

### 2. Normal Vector and General Form

- **Normal Vector:**
  A normal vector $\vec{n} = (n_x, n_y)$ is perpendicular to the direction vector $\vec{d} = (3, -3)$, meaning their dot product must be zero ($\vec{n} \cdot \vec{d} = 0$). Swapping the components of $\vec{d}$ and negating one gives:
  $$
  \vec{n} = (3, 3) \quad \text{or simplified:} \quad \vec{n} = (1, 1)
  $$
  Check orthogonality: $(1)(3) + (1)(-3) = 3 - 3 = 0$.

- **General Form ($Ax + By + C = 0$):**
  Using normal vector $\vec{n} = (1, 1)$ and base point $A=(1,2)$:
  $$
  1(x - 1) + 1(y - 2) = 0
  $$
  $$
  x - 1 + y - 2 = 0 \implies x + y - 3 = 0
  $$

---

### 3. Verification with Both Points

Substitute the coordinates of $A=(1,2)$ and $B=(4,-1)$ into the general equation $x + y - 3 = 0$:

- **Point $A=(1,2)$:**
  $$
  1 + 2 - 3 = 0 \quad (\text{True})
  $$

- **Point $B=(4,-1)$:**
  $$
  4 + (-1) - 3 = 3 - 3 = 0 \quad (\text{True})
  $$

- **Explanation & Reasoning:**
  A line in $\mathbb{R}^2$ is uniquely determined by a base point and either a parallel **direction vector** (for parametric representation) or a perpendicular **normal vector** (for general implicit representation). Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
