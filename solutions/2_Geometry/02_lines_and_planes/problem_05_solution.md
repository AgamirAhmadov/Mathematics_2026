# Lines and Planes

## Question

### Exercise 5. Relative Position of Two Lines
Analyze the position of

$$
L_1:(x,y,z)=(1,1,0)+t(1,2,1),
$$

$$
L_2:(x,y,z)=(2,0,1)+s(0,1,-1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

> **Why this exercise:** teaches how to distinguish qualitatively different relationships between lines in space.


## Solution

---

### 1. Check for Parallelism (Direction Vectors)

Extract the direction vectors from the parametric equations of both lines:
- Direction vector of $L_1$: $\vec{d}_1 = (1, 2, 1)$
- Direction vector of $L_2$: $\vec{d}_2 = (0, 1, -1)$

Check whether $\vec{d}_1$ and $\vec{d}_2$ are scalar multiples ($\vec{d}_1 = k\vec{d}_2$ for some $k \in \mathbb{R}$):
- Comparing the first components: $1 = k(0) \implies 1 = 0$, which is impossible.
- Therefore, $\vec{d}_1$ and $\vec{d}_2$ are **not proportional** (linearly independent), meaning the lines $L_1$ and $L_2$ are **not parallel** (and not coincident). They must either intersect at a single point or be skew.

---

### 2. Test for Intersection

To find a common intersection point, equate the corresponding $x$, $y$, and $z$ coordinates of $L_1$ and $L_2$:

$$
\begin{cases}
1 + t = 2 + 0s \\
1 + 2t = 0 + s \\
0 + t = 1 - s
\end{cases}
\implies
\begin{cases}
1 + t = 2 & \text{(1)} \\
1 + 2t = s & \text{(2)} \\
t = 1 - s & \text{(3)}
\end{cases}
$$

Solve the system using the first two equations:
1. From Equation (1):
   $$
   1 + t = 2 \implies t = 1
   $$
2. Substitute $t = 1$ into Equation (2) to find $s$:
   $$
   s = 1 + 2(1) = 3
   $$
3. Check whether $t = 1$ and $s = 3$ satisfy Equation (3):
   - Left-hand side: $t = 1$
   - Right-hand side: $1 - s = 1 - 3 = -2$
   - Comparison: $1 \neq -2$ (Contradiction)

- **Result:**
  - The overdetermined system of three equations in two unknowns ($t, s$) is **inconsistent**, meaning no pair $(t, s)$ satisfies all three coordinate equations simultaneously. Therefore, the lines **do not intersect**.

---

### 3. Classification and Justification

- **Classification:** The lines $L_1$ and $L_2$ are **skew**.
- **Justification:**
  In three-dimensional space ($\mathbb{R}^3$), two lines have four possible relative positions: coincident, parallel, intersecting, or skew.
  1. Because their direction vectors $\vec{d}_1 = (1, 2, 1)$ and $\vec{d}_2 = (0, 1, -1)$ are not scalar multiples of one another, the lines are neither parallel nor coincident.
  2. Because setting their parametric coordinates equal yields an inconsistent system with no common solution, the lines do not intersect.
  
  Two lines in space that are neither parallel nor intersecting are by definition **skew lines** (they lie in separate parallel planes and pass by one another without meeting), formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
