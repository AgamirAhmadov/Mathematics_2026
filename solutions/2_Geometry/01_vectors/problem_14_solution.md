# Vectors and Analytic Geometry

## Question

For $P=(4,1)$ and the line through the origin in direction $v=(1,2)$, find the closest point and distance using projection, and verify the relevant perpendicularity.


## Solution

---

### 1. Find the Closest Point Using Orthogonal Projection

The closest point $Q$ on the line passing through the origin in direction $\vec{v} = (1, 2)$ to the external point $P = (4, 1)$ is the orthogonal projection of the position vector $\vec{p} = (4, 1)$ onto $\vec{v}$:

$$
Q = \mathrm{proj}_{\vec{v}} \vec{p} = \frac{\vec{p} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}\vec{v}
$$

1. **Compute the dot products $\vec{p} \cdot \vec{v}$ and $\vec{v} \cdot \vec{v}$:**
   $$
   \vec{p} \cdot \vec{v} = (4)(1) + (1)(2) = 4 + 2 = 6
   $$
   $$
   \vec{v} \cdot \vec{v} = 1^2 + 2^2 = 1 + 4 = 5
   $$

2. **Compute the projection vector $Q$:**
   $$
   Q = \frac{6}{5}(1, 2) = \left(\frac{6}{5}, \; \frac{12}{5}\right)
   $$

- **Result:**
  - The closest point on the line is **$Q = \left(\frac{6}{5}, \frac{12}{5}\right)$**.

---

### 2. Compute the Distance Between $P$ and $Q$

First, find the perpendicular displacement vector $\overrightarrow{QP} = P - Q$ from the closest point $Q$ to $P$:

$$
P - Q = (4, 1) - \left(\frac{6}{5}, \; \frac{12}{5}\right) = \left(\frac{20}{5} - \frac{6}{5}, \; \frac{5}{5} - \frac{12}{5}\right) = \left(\frac{14}{5}, \; -\frac{7}{5}\right)
$$

Next, compute the Euclidean norm $\|P - Q\|$ to obtain the shortest distance:

$$
\|P - Q\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196 + 49}{25}} = \sqrt{\frac{245}{25}} = \frac{\sqrt{49 \cdot 5}}{5} = \frac{7\sqrt{5}}{5} = \frac{7}{\sqrt{5}}
$$

- **Result:**
  - The distance from $P$ to the line is **$\frac{7}{\sqrt{5}}$** (or rationalized as **$\frac{7\sqrt{5}}{5}$**).

---

### 3. Verify the Relevant Perpendicularity

To verify that the displacement segment $\overline{QP}$ is orthogonal to the line, compute the dot product of $P - Q$ with the line's direction vector $\vec{v} = (1, 2)$:

$$
(P - Q) \cdot \vec{v} = \left(\frac{14}{5}, \; -\frac{7}{5}\right) \cdot (1, 2) = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0
$$

- **Explanation & Reasoning:**
  Because $(P - Q) \cdot \vec{v} = 0$, the displacement vector $P - Q$ is strictly perpendicular to the direction of the line. By the Pythagorean theorem, for any other point $X$ on the line, the squared distance satisfies $\|P - X\|^2 = \|P - Q\|^2 + \|Q - X\|^2 \ge \|P - Q\|^2$, which guarantees that the orthogonal foot $Q$ is the unique closest point on the line to $P$, formatted cleanly for GitHub rendering in accordance with [hints.md](https://github.com/AgamirAhmadov/Mathematics_2026/blob/main/hints.md).
