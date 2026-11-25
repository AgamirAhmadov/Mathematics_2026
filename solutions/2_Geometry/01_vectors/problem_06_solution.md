# Vectors and Orthogonal Projections

## Question

Project $u=(4,2)$ onto $v=(1,1)$, compute the residual $r$, verify $r\cdot v=0$, and explain the result geometrically.


## Solution

---

### 1. Compute the Orthogonal Projection of $u$ onto $v$

The orthogonal projection of a vector $\vec{u} = (4, 2)$ onto a non-zero vector $\vec{v} = (1, 1)$ is given by:

$$
\mathrm{proj}_{\vec{v}} \vec{u} = \frac{\vec{u} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}\vec{v}
$$

1. **Compute the dot products $\vec{u} \cdot \vec{v}$ and $\vec{v} \cdot \vec{v}$:**
   $$
   \vec{u} \cdot \vec{v} = (4)(1) + (2)(1) = 4 + 2 = 6
   $$
   $$
   \vec{v} \cdot \vec{v} = 1^2 + 1^2 = 1 + 1 = 2
   $$

2. **Evaluate the projection vector:**
   $$
   \mathrm{proj}_{\vec{v}} \vec{u} = \frac{6}{2}(1, 1) = 3(1, 1) = (3, 3)
   $$

- **Result:**
  - The projection of $u$ onto $v$ is **$\mathrm{proj}_{\vec{v}} \vec{u} = (3, 3)$**.

---

### 2. Compute the Residual Vector $r$

The residual (orthogonal complement component) $\vec{r}$ is obtained by subtracting the projection from the original vector $\vec{u}$:

$$
\vec{r} = \vec{u} - \mathrm{proj}_{\vec{v}} \vec{u} = (4, 2) - (3, 3) = (4 - 3, \; 2 - 3) = (1, -1)
$$

- **Result:**
  - The residual vector is **$\vec{r} = (1, -1)$**.

---

### 3. Verify That $r \cdot v = 0$

Compute the dot product of $\vec{r} = (1, -1)$ and $\vec{v} = (1, 1)$:

$$
\vec{r} \cdot \vec{v} = (1)(1) + (-1)(1) = 1 - 1 = 0
$$

- **Result:**
  - Verified: **$\vec{r} \cdot \vec{v} = 0$**.

---

### 4. Geometric Explanation

- **Explanation & Reasoning:**
  The vector $\vec{u} = (4, 2)$ decomposes uniquely into two mutually orthogonal parts relative to the direction $\vec{v} = (1, 1)$:
  $$
  \vec{u} = \mathrm{proj}_{\vec{v}} \vec{u} + \vec{r} = (3, 3) + (1, -1)
  $$
  1. **Parallel component ($\mathrm{proj}_{\vec{v}} \vec{u} = (3, 3)$):** Because $(3, 3) = 3(1, 1)$ is a scalar multiple of $\vec{v}$, it lies along the line spanned by $\vec{v}$ and captures the shadow or forward reach of $\vec{u}$ in the direction of $\vec{v}$.
  2. **Perpendicular component ($\vec{r} = (1, -1)$):** Subtracting the parallel projection removes the movement along $\vec{v}$, leaving the sideways (orthogonal) displacement from the projected tip $(3, 3)$ to the tip of $\vec{u} = (4, 2)$. Because $\vec{r} \cdot \vec{v} = 0$, $\vec{r}$ meets $\vec{v}$ at a $90^\circ$ right angle, forming a right triangle with hypotenuse $\vec{u}$ and legs $(3, 3)$ and $(1, -1)$.

  Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
