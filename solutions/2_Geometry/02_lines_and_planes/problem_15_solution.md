# Lines and Planes

## Question

### Exercise 15. Complete Classification of a Line Relative to a Plane
Let

$$L:p+tv,\qquad \Pi:n\cdot x=d.$$

State the conditions distinguishing the three cases: one intersection point, parallel with no common points, and the line contained in the plane. Then illustrate each case with your own simple numerical example.

> **Why this exercise:** requires formulating a general mathematical criterion instead of carrying out one isolated calculation.


## Solution

---

### 1. General Classification Criteria

To find the intersection of the line $L : x(t) = p + tv$ ($t \in \mathbb{R}$, with direction vector $v \neq 0$) and the plane $\Pi : n \cdot x = d$ (with normal vector $n \neq 0$), substitute $x(t)$ into the plane equation:

$$n \cdot (p + tv) = d \implies (n \cdot v)t = d - n \cdot p$$

The number of solutions for $t$—and thus the geometric relationship between $L$ and $\Pi$—is completely determined by two scalar quantities: the dot product **$n \cdot v$** (orientation) and the incidence residual **$n \cdot p - d$** (whether the base point $p$ lies in $\Pi$).

| Relative Position | Orientation Condition | Incidence Condition | Algebraic Equation for $t$ |
| :--- | :--- | :--- | :--- |
| **1. One Intersection Point** | $n \cdot v \neq 0$ | Any $p \in \mathbb{R}^3$ | Unique solution $t = \dfrac{d - n \cdot p}{n \cdot v}$ |
| **2. Strictly Parallel (No Common Points)** | $n \cdot v = 0$ | $n \cdot p \neq d$ | Contradiction $0 \cdot t = d - n \cdot p \neq 0$ (no solution) |
| **3. Line Contained in the Plane** | $n \cdot v = 0$ | $n \cdot p = d$ | Identity $0 \cdot t = 0$ (infinitely many solutions, all $t \in \mathbb{R}$) |

---

### 2. Numerical Illustrations for Each Case

Use the fixed plane $\Pi : x + y + z = 3$, where $n = (1, 1, 1)$ and $d = 3$, for all three examples.

#### Case 1: One Intersection Point ($n \cdot v \neq 0$)
- **Example Line:** $L_1 : p + tv = (0, 0, 0) + t(1, 1, 1)$
- **Verify Conditions:**
  - $n \cdot v = (1, 1, 1) \cdot (1, 1, 1) = 1 + 1 + 1 = 3 \neq 0$
- **Intersection Calculation:**
  $$t = \frac{3 - (1, 1, 1) \cdot (0, 0, 0)}{3} = \frac{3 - 0}{3} = 1$$
  Substituting $t = 1$ into $L_1$ gives the unique intersection point **$(1, 1, 1)$**.

---
