# Lecture 2 - Elimination with Matrices

## Some Key Ideas

- This is a key concept in how software solves for linear systems.
- A **pivot** is the first nonzero element of a row in a matrix.

## Example - Basic solving of a system

> We are given 3 linear equations with 3 variables,

$$x+2y+z=2$$
$$3x+8y+z=12$$
$$4y+z=2$$

> This can be minimally represented with

$$\begin{bmatrix}
    1 & 2 & 1\\
    3 & 8 & 1\\
    0 & 4 & 1\\
\end{bmatrix}$$

The goal is to eliminate all variables for a given equation until there is only one.

For the first equation, the pivot is the constant multiplying the x variable, which is 1.

> To eliminate the x variable in the 2nd equation, one can take 3 times the 1st equation and subtract it from the 2nd, leaving

$$0x+2y-2z=6$$

> Which now makes the 2nd iteration of the matrix

$$\begin{bmatrix}
    1 & 2 & 1\\
    0 & 2 & -2\\
    0 & 4 & 1\\
\end{bmatrix}$$

> This can continue until the nth iteration of the matrix is sufficiently eliminated into row-echelon form, which looks like

$$\begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    0 & 0 & 1\\
\end{bmatrix}$$

## Represenetation with Matrices - *In Detail*

### Matrix Multiplication - 3x3 and 3x1

> Given

$$\begin{bmatrix}
    1 & 1 & 1\\
    2 & 2 & 2\\
    3 & 3 & 3\\
\end{bmatrix} \cdot \begin{bmatrix}
    3\\
    4\\
    5\\
\end{bmatrix}$$

The result is another 3x1 Matrix that is the sum of 3 times the first column (i.e. element 1 of right matrix), 4 times the second column, and 5 times the third column.

### Matrix Multiplication - 1x3 and 3x3

> Given

$$\begin{bmatrix}
    1 & 2 & 3\\
\end{bmatrix} \cdot \begin{bmatrix}
    1 & 2 & 3\\
    1 & 2 & 3\\
    4 & 5 & 6\\
\end{bmatrix}$$

The result is another 1x3 Matrix that is the sum of 1 times the first row, 2 times the second row, and 3 times the third row.

> With matrix

$$\begin{bmatrix}
    1 & 2 & 1\\
    3 & 8 & 1\\
    0 & 4 & 1\\
\end{bmatrix}$$

How do we subtract 3 times the value of row 1 from row 2?


$$?? \cdot \begin{bmatrix}
    1 & 2 & 1\\
    3 & 8 & 1\\
    0 & 4 & 1\\
\end{bmatrix}=\begin{bmatrix}
    1 & 2 & 1\\
    0 & 2 & -2\\
    0 & 4 & 1\\
\end{bmatrix}$$

> We can start with the identity matrix, which is a matrix that when multiplied with another matrix, leaves the result unchanged.

$$\begin{bmatrix}
    1 & 0 & 0\\
    0 & 1 & 0\\
    0 & 0 & 1\\
\end{bmatrix}$$

> So, the matrix could look like,

$$\begin{bmatrix}
    1 & 0 & 0\\
    -3 & 1 & 0\\
    0 & 0 & 1\\
\end{bmatrix}$$

### Matrix Notation

> The matrix determined above is called an *Elementary Matrix*, which can be noted as

$$E_{21}=\begin{bmatrix}
    1 & 0 & 0\\
    -3 & 1 & 0\\
    0 & 0 & 1\\
\end{bmatrix}$$

It means that the elementary matrix was used to fix the (2, 1) element, that is to turn it to 0.

### Finding the matrix that eliminates in one step

> That matrix is just the composition of each of the smaller steps determined before,

$$E_{32}(E_{21}A)=U$$

**NOTE:** Matrix multiplication is not commutative, which means that **order matters**.

### Permutation Matrices

What matrix exchanges two rows of another matrix when multiplied together?

$$?? \cdot \begin{bmatrix}
    a & b\\
    c & d\\
\end{bmatrix}=\begin{bmatrix}
    c & d\\
    a & b\\
\end{bmatrix}$$

> That matrix is

$$\begin{bmatrix}
    0 & 1\\
    1 & 0\\
\end{bmatrix}$$

> To switch columns, simply multiply the permutation matrix after the matrix you want to transform, like this

$$\begin{bmatrix}
    a & b\\
    c & d\\
\end{bmatrix} \cdot \begin{bmatrix}
    0 & 1\\
    1 & 0\\
\end{bmatrix}=\begin{bmatrix}
    b & a\\
    d & c\\
\end{bmatrix}$$

### Matrix Inverses

> Generally,

$$A \cdot A^{-1}=\begin{bmatrix}
    1 & 0\\
    0 & 1\\
\end{bmatrix}$$