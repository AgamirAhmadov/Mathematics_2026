## Question

### Exercise 7. Inverse of a Product
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.


## Solution

To study how inverses interact with matrix multiplication, we verify the fundamental product property: **$(AB)^{-1} = B^{-1}A^{-1}$**. We will compute the product matrix first, invert it, and then compare it to the product of the individual inverses taken in reverse order.

---

### 1. Compute the Product Matrix $AB$ and Its Inverse $(AB)^{-1}$

- **Matrix Product $AB$:**
  $$
  AB = \begin{pmatrix}
  1 & 1 \\
  0 & 1
  \end{pmatrix}
  \begin{pmatrix}
  2 & 0 \\
  0 & 3
  \end{pmatrix}
  = \begin{pmatrix}
  (1)(2) + (1)(0) & (1)(0) + (1)(3) \\
  (0)(2) + (1)(0) & (0)(0) + (1)(3)
  \end{pmatrix}
  = \begin{pmatrix}
  2 & 3 \\
  0 & 3
  \end{pmatrix}
  $$

- **Inverse Formula for a $2 \times 2$ Matrix:**
  For $X = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, $X^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$.
  Here, for $AB$, $a = 2, b = 3, c = 0, d = 3$:
  $$
  \det(AB) = (2)(3) - (3)(0) = 6 - 0 = 6
  $$

- **Result for $(AB)^{-1}$:**
  $$
  (AB)^{-1} = \frac{1}{6} \begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{6} & -\frac{3}{6} \\ 0 & \frac{2}{6} \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
  $$

---

### 2. Compute the Individual Inverses $A^{-1}$ and $B^{-1}$

- **Inverse of $A$:**
  Using $\det(A) = (1)(1) - (1)(0) = 1$:
  $$
  A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}
  $$

- **Inverse of $B$:**
  Using $\det(B) = (2)(3) - (0)(0) = 6$:
  $$
  B^{-1} = \frac{1}{6} \begin{pmatrix} 3 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{6} & 0 \\ 0 & \frac{2}{6} \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix}
  $$

---

### 3. Compute the Product in Reverse Order $B^{-1}A^{-1}$

- **Calculation:**
  $$
  B^{-1}A^{-1} = \begin{pmatrix}
  \frac{1}{2} & 0 \\
  0 & \frac{1}{3}
  \end{pmatrix}
  \begin{pmatrix}
  1 & -1 \\
  0 & 1
  \end{pmatrix}
  = \begin{pmatrix}
  \left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\
  (0)(1) + \left(\frac{1}{3}\right)(0) & (0)(-1) + \left(\frac{1}{3}\right)(1)
  \end{pmatrix}
  $$

- **Result:**
  $$
  B^{-1}A^{-1} = \begin{pmatrix}
  \frac{1}{2} & -\frac{1}{2} \\
  0 & \frac{1}{3}
  \end{pmatrix}
  $$

---

### 4. Comparison and Explanation of the Reversed Order

- **Verification:**
  Comparing our results from Step 1 and Step 3, we find:
  $$
  (AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
  $$

- **Explanation & Reasoning:**
  Matrix multiplication represents a sequence of linear transformations applied one after another. When you apply transformation $A$ followed by transformation $B$ (written as $AB$), undoing the combined operation requires reversing them in the exact opposite sequence. 

  Think of putting on socks and then shoes: to undo the process, you must take off your shoes first ($B^{-1}$) and then your socks ($A^{-1}$). Similarly, the inverse of a combined transformation product must be applied in reverse order to properly cancel out each transformation step.
