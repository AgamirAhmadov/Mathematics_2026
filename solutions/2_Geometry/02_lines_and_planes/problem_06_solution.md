# Lines and Planes

## Question

### Exercise 6. Angle Between Planes
Given

$$
\Pi_1:x+y+z=1,\qquad \Pi_2:x-y=2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

> **Why this exercise:** focuses attention on one mechanism—using normals to analyze position and angle—without also introducing the construction of the intersection line.


## Solution

---

### 1. Extract Normal Vectors and Test for Parallelism

From the general plane equation $Ax + By + Cz = D$, the coefficients of $x, y, z$ directly give the normal vector $\vec{n} = (A, B, C)$:

- **Normal vector of $\Pi_1$ ($x + y + z = 1$):**
  $$
  \vec{n}_1 = (1, 1, 1)
  $$

- **Normal vector of $\Pi_2$ ($x - y + 0z = 2$):**
  $$
  \vec{n}_2 = (1, -1, 0)
  $$

#### Parallelism Check:
Two planes are parallel if and only if their normal vectors are scalar multiples of one another ($\vec{n}_1 = k\vec{n}_2$ for some $k \in \mathbb{R}$):
- Comparing the third components: $1 = k(0) \implies 1 = 0$, which is impossible.
- Comparing the first two components also yields conflicting ratios ($\frac{1}{1} = 1 \neq \frac{1}{-1} = -1$).

- **Result:**
  Since $\vec{n}_1$ and $\vec{n}_2$ are not proportional, **the planes $\Pi_1$ and $\Pi_2$ are not parallel** (they intersect along a line).

---

### 2. Compute the Angle Between the Planes

The acute angle $\theta \in [0, \frac{\pi}{2}]$ between two intersecting planes equals the acute angle between their normal vectors, given by the dot product formula:

$$
\cos\theta = \frac{|\vec{n}_1 \cdot \vec{n}_2|}{\|\vec{n}_1\| \|\vec{n}_2\|}
$$

1. **Compute the dot product $\vec{n}_1 \cdot \vec{n}_2$:**
   $$
   \vec{n}_1 \cdot \vec{n}_2 = (1)(1) + (1)(-1) + (1)(0) = 1 - 1 + 0 = 0
   $$

2. **Compute the magnitudes $\|\vec{n}_1\|$ and $\|\vec{n}_2\|$:**
   $$
   \|\vec{n}_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}
   $$
   $$
   \|\vec{n}_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{2}
   $$

3. **Solve for $\theta$:**
   $$
   \cos\theta = \frac{|0|}{\sqrt{3}\sqrt{2}} = 0 \implies \theta = \arccos(0) = \frac{\pi}{2} \text{ radians } (90^\circ)
   $$

- **Result:**
  The angle between $\Pi_1$ and $\Pi_2$ is **$90^\circ$ ($\frac{\pi}{2}$ radians)**, meaning the two planes are **perpendicular (orthogonal)**.

---

### 3. Why Normal Vectors Alone Are Sufficient

- **Explanation & Reasoning:**
  In three-dimensional space ($\mathbb{R}^3$), each normal vector $\vec{n}_i$ is strictly perpendicular ($90^\circ$) to every line and vector lying within its respective plane $\Pi_i$. 
  
  When two planes intersect at a dihedral angle $\theta$, rotating one plane into the other by $\theta$ around their line of intersection simultaneously rotates its perpendicular normal vector by the exact same angle $\theta$. Because the constant term $D$ in $Ax + By + Cz = D$ only shifts a plane parallel to itself without changing its spatial orientation or tilt, the normal vectors $\vec{n}_1$ and $\vec{n}_2$ completely capture the relative angular orientation of the planes—making it unnecessary to find their line of intersection first. Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
