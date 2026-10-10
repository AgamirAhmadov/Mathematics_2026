### Exercise 3. When Can Matrices Be Multiplied?
The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.


# Solution

## Exercise 3. When Can Matrices Be Multiplied?

Given the matrix sizes:

$$
A_{2\times3}, \qquad B_{3\times4}, \qquad C_{4\times2}, \qquad D_{2\times2}
$$

---

### Dimension Compatibility Rule

For a matrix product $XY$, where matrix $X$ has dimensions $m \times n$ and matrix $Y$ has dimensions $p \times q$, the product is **defined** if and only if the number of columns of $X$ equals the number of rows of $Y$ (i.e., $n = p$). When defined, the resulting matrix has dimensions $m \times q$ (outer dimensions).

---

### Analysis of Products

#### 1. Product $AB$
* **Dimensions:** $A_{2 \times 3}$ and $B_{3 \times 4}$
* **Result:** **Defined**, with size **$2 \times 4$**.
* **Justification:** The inner dimensions match ($3 = 3$). The resulting matrix takes the outer dimensions ($2 \times 4$).

#### 2. Product $BA$
* **Dimensions:** $B_{3 \times 4}$ and $A_{2 \times 3}$
* **Result:** **Not Defined**.
* **Justification:** The inner dimensions do not match ($4 \neq 2$). You cannot multiply a $3 \times 4$ matrix by a $2 \times 3$ matrix.

#### 3. Product $BC$
* **Dimensions:** $B_{3 \times 4}$ and $C_{4 \times 2}$
* **Result:** **Defined**, with size **$3 \times 2$**.
* **Justification:** The inner dimensions match ($4 = 4$). The resulting matrix takes the outer dimensions ($3 \times 2$).

#### 4. Product $CB$
* **Dimensions:** $C_{4 \times 2}$ and $B_{3 \times 4}$
* **Result:** **Not Defined**.
* **Justification:** The inner dimensions do not match ($2 \neq 3$).

#### 5. Product $AC$
* **Dimensions:** $A_{2 \times 3}$ and $C_{4 \times 2}$
* **Result:** **Not Defined**.
* **Justification:** The inner dimensions do not match ($3 \neq 4$).

#### 6. Product $CA$
* **Dimensions:** $C_{4 \times 2}$ and $A_{2 \times 3}$
* **Result:** **Defined**, with size **$4 \times 3$**.
* **Justification:** The inner dimensions match ($2 = 2$). The resulting matrix takes the outer dimensions ($4 \times 3$).

#### 7. Product $AD$
* **Dimensions:** $A_{2 \times 3}$ and $D_{2 \times 2}$
* **Result:** **Not Defined**.
* **Justification:** The inner dimensions do not match ($3 \neq 2$).

#### 8. Product $DA$
* **Dimensions:** $D_{2 \times 2}$ and $A_{2 \times 3}$
* **Result:** **Defined**, with size **$2 \times 3$**.
* **Justification:** The inner dimensions match ($2 = 2$). The resulting matrix takes the outer dimensions ($2 \times 3$).
