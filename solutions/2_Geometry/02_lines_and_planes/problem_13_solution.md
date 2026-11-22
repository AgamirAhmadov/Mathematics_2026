# Lines and Planes

## Question

### Exercise 13. Closest Point on a Plane
Find the point on the plane $x+2y+2z=4$ closest to $P=(3,0,0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

> **Why this exercise:** combines projection, distance, and the normal direction in one problem.


## Solution

---

### 1. Construct the Normal Line Through $P$

The closest point $Q$ on a plane $\Pi$ to an external point $P = (3, 0, 0)$ is the orthogonal projection of $P$ onto $\Pi$. It lies at the intersection of $\Pi$ with the line $L$ passing through $P$ parallel to the plane's normal vector:

- **Normal Vector of Plane $\Pi$ ($x + 2y + 2z = 4$):**
  $$
  \vec{n} = (1, 2, 2)
  $$

- **Parametric Equations of the Perpendicular Line $L$:**
  Using base point $P = (3, 0, 0)$ and direction vector $\vec{n} = (1, 2, 2)$ with parameter $t \in \mathbb{R}$:
  $$
  \begin{cases}
  x = 3 + t, \\
  y = 2t, \\
  z = 2t.
  \end{cases}
  $$

---

### 2. Find the Closest Point $Q$ on the Plane

Substitute the parametric coordinates of $L$ into the plane equation $x + 2y + 2z = 4$:

$$
(3 + t) + 2(2t) + 2(2t) = 4
$$

Combine like terms and solve for $t$:

$$
3 + (1 + 4 + 4)t = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}
$$

Substitute $t = \frac{1}{9}$ back into the parametric equations of $L$ to find $Q$:

$$
Q = \left(3 + \frac{1}{9}, \; 2\left(\frac{1}{9}\right), \; 2\left(\frac{1}{9}\right)\right) = \left(\frac{28}{9}, \; \frac{2}{9}, \; \frac{2}{9}\right)
$$

- **Result:**
  - The closest point on the plane is **$Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)$**.

---

### 3. Compute the Distance Between $P$ and $Q$

Compute the Euclidean distance $\|\overrightarrow{PQ}\|$ directly from $P = (3, 0, 0)$ to $Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)$:

$$
\overrightarrow{PQ} = Q - P = \left(\frac{28}{9} - 3, \; \frac{2}{9} - 0, \; \frac{2}{9} - 0\right) = \left(\frac{1}{9}, \; \frac{2}{9}, \; \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2)
$$

$$
d(P, Q) = \|\overrightarrow{PQ}\| = \sqrt{\left(\frac{1}{9}\right)^2 + \left(\frac{2}{9}\right)^2 + \left(\frac{2}{9}\right)^2} = \frac{1}{9}\sqrt{1 + 4 + 4} = \frac{1}{9}\sqrt{9} = \frac{3}{9} = \frac{1}{3}
$$

*(Cross-check via the point-to-plane distance formula: $D = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|-1|}{3} = \frac{1}{3}$.)*

- **Result:**
  - The distance from $P$ to the plane is **$\frac{1}{3}$**.

---

### 4. Check That Segment $\overline{PQ}$ Is Perpendicular to the Plane

A line segment is perpendicular to a plane if and only if its direction vector is parallel (a non-zero scalar multiple) to the plane's normal vector $\vec{n}$:

- Segment vector: $\overrightarrow{PQ} = \left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2)$
- Normal vector of $\Pi$: $\vec{n} = (1, 2, 2)$

Since $\overrightarrow{PQ} = \frac{1}{9}\vec{n}$, the segment $\overline{PQ}$ is strictly parallel to the normal vector $\vec{n}$, and therefore **perpendicular to the plane $\Pi$** (equivalently, its dot product with any vector in $\Pi$ is zero).

- **Explanation & Reasoning:**
  Minimizing distance from a point to a flat plane requires moving strictly along the normal direction $\vec{n}$, which is orthogonal to every direction within the plane. Because $\overrightarrow{PQ}$ is a positive scalar multiple of $\vec{n}$, it follows the shortest perpendicular path from $P$ to $\Pi$, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
