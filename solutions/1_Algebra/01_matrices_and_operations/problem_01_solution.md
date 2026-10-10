# Matrices and Basic Operations

### Exercise 1. Matrix Size and Entries
Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1 \\
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.


## Solution Matrix Size and Entries

Let the matrices $A$ and $B$ be defined as follows:

$$
A = \begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5
\end{pmatrix}, \qquad 
B = \begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1
\end{pmatrix}
$$

---

### 1. State the sizes of matrices $A$ and $B$.

- **Result:** 
  - Matrix $A$ is of size **$2 \times 3$**.
  - Matrix $B$ is of size **$3 \times 2$**.

- **Main Steps:**
  1. Count the number of horizontal rows ($m$) and vertical columns ($n$) for each matrix.
  2. Express the dimensions in the standard format $m \times n$ (rows $\times$ columns).

- **Explanation:** 
  A matrix's size (or dimension) is always defined by the number of rows followed by the number of columns. Matrix $A$ has 2 rows and 3 columns, while matrix $B$ has 3 rows and 2 columns.

---

### 2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.

- **Result:**
  - $a_{12} = -1$
  - $a_{23} = 5$
  - $b_{21} = -2$
  - $b_{32} = 1$

- **Main Steps:**
  1. Use the standard index notation $a_{ij}$, where $i$ denotes the row number and $j$ denotes the column number.
  2. Locate row 1, column 2 in $A$ to find $-1$.
  3. Locate row 2, column 3 in $A$ to find $5$.
  4. Locate row 2, column 1 in $B$ to find $-2$.
  5. Locate row 3, column 2 in $B$ to find $1$.

- **Explanation:** 
  Matrix entries are indexed by their row and column coordinates. The first subscript specifies the row (counting top to bottom), and the second subscript specifies the column (counting left to right).

---

### 3. Write the second row of $A$ and the first column of $B$ as vectors.

- **Result:**
  - Second row of $A$ as a row vector: $\begin{pmatrix} 0 & 4 & 5 \end{pmatrix}$
  - First column of $B$ as a column vector: $\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}$

- **Main Steps:**
  1. Extract all elements from the specified row or column in their respective order.
  2. Format them into a vector structure matching their orientation (horizontal for rows, vertical for columns).

- **Mathematical Verification:**
  Checking back against the original matrices confirms that the extracted elements correspond precisely to the specified row and column vectors without index shifts or omissions.
