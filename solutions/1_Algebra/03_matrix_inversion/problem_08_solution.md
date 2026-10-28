## Question

### Exercise 8. Inverse of a Transformation
The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.


## Solution

To find the inverse of the scaling matrix $S$, we can use the explicit $2 \times 2$ inverse formula or apply our understanding of diagonal matrices. For any diagonal matrix, the inverse is formed simply by reciprocating each element along the main diagonal.

---

### 1. Find $S^{-1}$

- **Determinant Calculation:**
  For $S = \begin{pmatrix} a & 0 \\ 0 & d \end{pmatrix}$, the determinant is $\det(S) = ad - bc = (2)\left(\frac{1}{2}\right) - (0)(0) = 1 - 0 = 1$.

- **Explicit Formula Application:**
  $$
  S^{-1} = \frac{1}{\det(S)} \begin{pmatrix} d & 0 \\ 0 & a \end{pmatrix} = \frac{1}{1} \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}
  $$

- **Explanation & Reasoning:**
  Because the determinant is $1$, scaling space through $S$ preserves area, and its inverse matrix $S^{-1}$ is straightforwardly constructed by inverting each diagonal entry (replacing $2$ with $\frac{1}{2}$ and $\frac{1}{2}$ with $2$).

---

### 2. Geometric Interpretation of the Inverse Transformation

- **Original Transformation ($S$):**
  Matrix $S$ stretches the horizontal $x$-coordinate by a factor of $2$ and compresses the vertical $y$-coordinate by a factor of $\frac{1}{2}$ ($\times 0.5$).

- **Inverse Transformation ($S^{-1}$):**
  Matrix $S^{-1}$ performs the exact opposite geometric operations: it compresses the $x$-coordinate by a factor of $\frac{1}{2}$ (dividing by $2$) and stretches the $y$-coordinate by a factor of $2$ ($\times 2$). 

- **Explanation & Reasoning:**
  Geometrically, an inverse matrix completely reverses or "undoes" whatever geometric transformation the original matrix performed, returning every point in the plane back to its original coordinates.

---

### 3. Check the Action on a Simple Vector

Let us choose a simple test vector $v = \begin{pmatrix} 4 \\ 6 \end{pmatrix}$.

- **Step A: Apply the scaling matrix $S$ to vector $v$:**
  $$
  Sv = \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 4 \\ 6 \end{pmatrix} = \begin{pmatrix} (2)(4) + (0)(6) \\ (0)(4) + \left(\frac{1}{2}\right)(6) \end{pmatrix} = \begin{pmatrix} 8 \\ 3 \end{pmatrix}
  $$
  *(The $x$-component doubled to $8$, and the $y$-component halved to $3$.)*

- **Step B: Apply the inverse matrix $S^{-1}$ to the resulting vector:**
  $$
  S^{-1}(Sv) = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 8 \\ 3 \end{pmatrix} = \begin{pmatrix} \left(\frac{1}{2}\right)(8) + (0)(3) \\ (0)(8) + (2)(3) \end{pmatrix} = \begin{pmatrix} 4 \\ 6 \end{pmatrix} = v
  $$

- **Explanation & Reasoning:**
  Multiplying the vector by $S$ transformed it, and subsequently applying $S^{-1}$ completely undid that transformation, restoring the vector to its exact starting point $v$. This confirms that $S^{-1}S = I$.
