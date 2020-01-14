# 2 Linear Equations in 2D

We have

$$2x-y=0$$
$$-x+2y=3$$

We can turn these equations into a 2x2 matrix:

$$\begin{bmatrix}
    2 & -1\\
    -1 & 2\\
\end{bmatrix} \cdot \begin{bmatrix}
    x \\
    y \\
\end{bmatrix}=\begin{bmatrix}
    0 \\
    3 \\
\end{bmatrix}$$

$$Ax=B$$

The matrices are A, X, and B, respectively
This can be rearranged to become a **Linear Combination**:

$$x\cdot \begin{bmatrix}
    2\\
    -1\\
\end{bmatrix} + y\cdot \begin{bmatrix}
    -1\\
    2\\
\end{bmatrix}=\begin{bmatrix}
    0\\
    3\\
\end{bmatrix}$$

The set of x and y that satisfies that equality is the point of intersection of the system of linear equations.

# 3 Linear Equations in 3D

> Given that

$$2x-y=0$$
$$-x+2y-z=-1$$
$$-3y+4z=4$$

> Let A and B equal:

$$A=\begin{bmatrix}
    2 & -1 & 0\\
    -1 & 2 & -1\\
    0 & -3 & 4\\
\end{bmatrix}$$

$$x=\begin{bmatrix}
    x\\
    y\\
    z\\
\end{bmatrix}$$

$$B=\begin{bmatrix}
    0\\
    -1\\
    4\\
\end{bmatrix}$$

For the equation corresponding to the second row of A, imagine a plane representing all solutions to the equation.
Now, imagine each equation corresponding to each row of the matrix has a plane of solutions.
The intersection of the three planes is a **point**.

Now,

$$Ax=B$$

becomes

$$x \cdot \begin{bmatrix}
    2\\
    -1\\
    0\\
\end{bmatrix} + y \cdot \begin{bmatrix}
    -1\\
    2\\
    -1\\
\end{bmatrix} + z \cdot \begin{bmatrix}
    0\\
    -1\\
    4\\
\end{bmatrix}=\begin{bmatrix}
    0\\
    -1\\
    4\\
\end{bmatrix}$$

For the equality to be satisfied x=0, y=0, z=1

# Interdependence

When two or more vectors lie in the same plane, their span is limited to that plane.
Those vectors are linearly dependent of each other.

# Tips for Visualizing Matrix Multiplication

> To multiply this,

$$\begin{bmatrix}
    2 & 5\\
    1 & 3\\
\end{bmatrix} \begin{bmatrix}
    1\\
    2\\
\end{bmatrix}$$

> picture that you are taking 1 of the first column and 2 of the second column and adding the results together:

$$1\cdot \begin{bmatrix}
    2\\
    1\\
\end{bmatrix} + 2\cdot \begin{bmatrix}
    5\\
    3\\
\end{bmatrix}=\begin{bmatrix}
    2 + 2 * 5\\
    1 + 2 * 3\\
\end{bmatrix}=\begin{bmatrix}
    12\\
    7\\
\end{bmatrix}$$
