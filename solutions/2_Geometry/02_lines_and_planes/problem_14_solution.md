# Lines and Planes

## Question

### Exercise 14. Contrast: Intersection and Parallelism
From the point $P=(0,0,1)$, two lines are drawn with direction vectors

$$
v_1=(2,1,-1),\qquad v_2=(2,1,0).
$$

For each line, analyze its position relative to the plane $z=0$.

For the line that intersects the plane, find the intersection point. For the other line, explain how you can recognize parallelism without solving an equation.

> **Why this exercise:** compares two very similar data sets that lead to different outcomes and forces recognition of the geometric condition before calculation.


## Solution

---

### 1. Geometric Setup: Lines and Plane Normal

From the base point $P = (0, 0, 1)$, write the parametric equations of both lines ($t, s \in \mathbb{R}$) and identify the normal vector of the plane $\Pi : z = 0$:

- **Plane $\Pi$ ($0x + 0y + 1z = 0$):**
  - Normal vector: $\vec{n} = (0, 0, 1)$

- **Line $L_1$ (direction $\vec{v}_1 = (2, 1, -1)$):**
  $$
  L_1 : (x, y, z) = (0, 0, 1) + t(2, 1, -1) \implies
  \begin{cases}
  x = 2t, \\
  y = t, \\
  z = 1 - t.
  \end{cases}
  $$

- **Line $L_2$ (direction $\vec{v}_2 = (2, 1, 0)$):**
  $$
  L_2 : (x, y, z) = (0, 0, 1) + s(2, 1, 0) \implies
  \begin{cases}
  x = 2s, \\
  y = s, \\
  z = 1.
  \end{cases}
  $$

---

### 2. Relative Position Analysis Using the Dot Product ($\vec{v}_i \cdot \vec{n}$)

Test the dot product between each line's direction vector and the plane's normal vector $\vec{n} = (0, 0, 1)$:

- **For Line $L_1$:**
  $$
  \vec{v}_1 \cdot \vec{n} = (2)(0) + (1)(0) + (-1)(1) = -1 \neq 0
  $$
  Since $\vec{v}_1 \cdot \vec{n} \neq 0$, the direction vector $\vec{v}_1$ is not orthogonal to $\vec{n}$. Therefore, **$L_1$ intersects the plane $z = 0$ at a single unique point**.

- **For Line $L_2$:**
  $$
  \vec{v}_2 \cdot \vec{n} = (2)(0) + (1)(0) + (0)(1) = 0
  $$
  Since $\vec{v}_2 \cdot \vec{n} = 0$, the direction vector $\vec{v}_2$ is perpendicular to $\vec{n}$ (parallel to the plane). Furthermore, the base point $P = (0, 0, 1)$ has $z$-coordinate $1 \neq 0$, meaning $P$ does not lie on the plane $z = 0$. Therefore, **$L_2$ is strictly parallel to the plane $z = 0$ and never intersects it**.

---

### 3. Find the Intersection Point for $L_1$

Substitute the $z$-coordinate of $L_1$ ($z = 1 - t$) into the plane equation $z = 0$:

$$
1 - t = 0 \implies t = 1
$$

Substitute $t = 1$ back into the parametric equations of $L_1$ to find the intersection point $Q$:

$$
Q = (0, 0, 1) + 1(2, 1, -1) = (2, 1, 0)
$$

- **Verification:**
  - $Q = (2, 1, 0)$ has $z = 0$ (lies on $\Pi$) and corresponds to $t = 1$ on $L_1$.
- **Result:**
  - The intersection point of $L_1$ with the plane $z = 0$ is **$Q = (2, 1, 0)$**.

---

### 4. Recognizing Parallelism for $L_2$ Without Solving an Equation

- **Explanation & Reasoning:**
  You can immediately recognize that $L_2$ is parallel to the plane $z = 0$ without setting up or solving any algebraic equation by inspecting its **direction vector** $\vec{v}_2 = (2, 1, 0)$:
  1. **Zero $z$-component in $\vec{v}_2$:** The third component of $\vec{v}_2$ is $0$, which means moving along $L_2$ produces **zero change in height** ($\Delta z = 0$). Because the plane $z = 0$ is the horizontal $xy$-plane (whose normal vector is $\vec{n} = (0, 0, 1)$), any direction vector with a zero $z$-component has $\vec{v}_2 \cdot \vec{n} = 0$ and is purely horizontal.
  2. **Non-zero initial height at $P$:** Since the line starts at $P = (0, 0, 1)$ at height $z = 1$ and never changes its $z$-coordinate, it remains at a constant distance of $1$ unit above the plane $z = 0$ everywhere—confirming strict parallelism at a glance, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
