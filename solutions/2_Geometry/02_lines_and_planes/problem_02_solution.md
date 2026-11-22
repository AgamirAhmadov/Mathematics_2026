# Analytic Geometry in the Plane and Space

## Question

### Exercise 2. A Line in Space
Given

$$
L:(x,y,z)=(2,-1,3)+t(1,2,-2).
$$

State a point on the line and its direction vector, check whether $P=(4,3,-1)$ lies on $L$, and find the point corresponding to $t=-1$.

> **Why this exercise:** reinforces the interpretation of parametric form as “point + direction.”


## Solution

---

### 1. Base Point and Direction Vector

From the vector equation $L : \mathbf{r}(t) = \mathbf{r}_0 + t\mathbf{d}$, we read the components directly:

- **A Point on the Line ($t = 0$):**
  $$
  P_0 = (2, -1, 3)
  $$

- **Direction Vector:**
  $$
  \vec{d} = (1, 2, -2)
  $$

---

### 2. Check Whether $P = (4, 3, -1)$ Lies on $L$

For $P = (4, 3, -1)$ to lie on $L$, there must exist a single scalar parameter $t \in \mathbb{R}$ that satisfies all three coordinate equations simultaneously:

$$
\begin{cases}
2 + t = 4, \\
-1 + 2t = 3, \\
3 - 2t = -1.
\end{cases}
$$

Solve each coordinate equation for $t$:
1. **x-coordinate:** $2 + t = 4 \implies t = 2$
2. **y-coordinate:** $-1 + 2t = 3 \implies 2t = 4 \implies t = 2$
3. **z-coordinate:** $3 - 2t = -1 \implies -2t = -4 \implies t = 2$

- **Result:**
  Since all three equations yield the exact same parameter value **$t = 2$**, the point **$P = (4, 3, -1)$ lies on $L$**.

---

### 3. Find the Point Corresponding to $t = -1$

Substitute $t = -1$ into the parametric equation of line $L$:

$$
(x, y, z) = (2, -1, 3) + (-1)(1, 2, -2)
$$

$$
(x, y, z) = (2 - 1, -1 - 2, 3 + 2) = (1, -3, 5)
$$

- **Result:**
  The point corresponding to $t = -1$ is **$(1, -3, 5)$**.

---

### 4. Explanation & Reasoning

The parametric equation $(x, y, z) = \mathbf{r}_0 + t\vec{d}$ describes a line in $\mathbb{R}^3$ by starting at a fixed position $\mathbf{r}_0 = (2, -1, 3)$ and moving along the direction vector $\vec{d} = (1, 2, -2)$ scaled by $t$. A point lies on the line if and only if a single consistent parameter $t$ generates all three of its coordinates simultaneously. Formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
