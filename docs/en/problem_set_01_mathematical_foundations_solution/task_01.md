# Task 01 – Vectors and linear transformations

## Problem Statement

Given two vectors in three-dimensional space:

$$
\vec a = (2,-1,3), \qquad \vec b = (1,4,-2)
$$

And the matrix:

$$
A =
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
$$

Determine:
1. The lengths $|\vec a|$, $|\vec b|$.
2. The normalized vector $\hat a$.
3. The dot product $\vec a \cdot \vec b$ and the angle between the vectors.
4. The cross product $\vec a \times \vec b$ and the area of the parallelogram spanned by these vectors.
5. The product $A\vec a$.
6. The determinant $\det A$ and whether the transformation preserves the orientation of the space.

## Theory

The length (magnitude) of a vector in Euclidean space is given by the square root of the sum of the squares of its components.

Normalization involves scaling a vector by the reciprocal of its length to create a unit vector.

The dot product yields a scalar and relates to the angle $\theta$ between vectors via:

$$
\cos\theta = \frac{\vec a \cdot \vec b}{|\vec a||\vec b|}
$$

The cross product yields a vector orthogonal to both operands. Its magnitude corresponds to the area of the parallelogram spanned by the two vectors.

The determinant of a transformation matrix indicates how the transformation scales volumes. A positive determinant implies that the transformation preserves the spatial orientation (right-handedness).

## Step-by-Step Solution

### 1. Lengths of the vectors

$$
\begin{align}
|\vec a| &= \sqrt{2^2 + (-1)^2 + 3^2} \\
         &= \sqrt{4 + 1 + 9} \\
         &= \sqrt{14}
\end{align}
$$

$$
\begin{align}
|\vec b| &= \sqrt{1^2 + 4^2 + (-2)^2} \\
         &= \sqrt{1 + 16 + 4} \\
         &= \sqrt{21}
\end{align}
$$

### 2. Normalized vector

$$
\begin{align}
\hat a &= \frac{1}{|\vec a|} \vec a \\
       &= \frac{1}{\sqrt{14}} (2, -1, 3) \\
       &= \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)
\end{align}
$$

### 3. Dot product and angle

$$
\begin{align}
\vec a \cdot \vec b &= (2)(1) + (-1)(4) + (3)(-2) \\
                    &= 2 - 4 - 6 \\
                    &= -8
\end{align}
$$

The angle $\theta$ is derived from the dot product relation:

$$
\cos\theta = \frac{-8}{\sqrt{14}\sqrt{21}}
$$

$$
\cos\theta = \frac{-8}{7\sqrt{6}}
$$

$$
\theta = \arccos\left(\frac{-8}{7\sqrt{6}}\right)
$$

### 4. Cross product and parallelogram area

$$
\begin{align}
\vec a \times \vec b &= \bigl((-1)(-2) - (3)(4), (3)(1) - (2)(-2), (2)(4) - (-1)(1)\bigr) \\
                     &= (2 - 12, 3 + 4, 8 + 1) \\
                     &= (-10, 7, 9)
\end{align}
$$

The area of the parallelogram is the magnitude of this vector:

$$
\begin{align}
\text{Area} &= |\vec a \times \vec b| \\
            &= \sqrt{(-10)^2 + 7^2 + 9^2} \\
            &= \sqrt{100 + 49 + 81} \\
            &= \sqrt{230}
\end{align}
$$

### 5. Matrix-vector multiplication

$$
\begin{align}
A\vec a &=
\begin{pmatrix}
2 & 1 & 0 \\
0 & 1 & -1 \\
1 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
2 \\
-1 \\
3
\end{pmatrix} \\
&=
\begin{pmatrix}
2(2) + 1(-1) + 0(3) \\
0(2) + 1(-1) - 1(3) \\
1(2) + 0(-1) + 1(3)
\end{pmatrix} \\
&=
\begin{pmatrix}
3 \\
-4 \\
5
\end{pmatrix}
\end{align}
$$

### 6. Determinant and orientation

Expanding the determinant along the first row:

$$
\begin{align}
\det A &= 2(1 \cdot 1 - (-1) \cdot 0) - 1(0 \cdot 1 - (-1) \cdot 1) + 0 \\
       &= 2(1) - 1(1) \\
       &= 1
\end{align}
$$

## Final Result

- $|\vec a| = \sqrt{14}$
- $|\vec b| = \sqrt{21}$
- $\hat a = \left( \frac{2}{\sqrt{14}}, \frac{-1}{\sqrt{14}}, \frac{3}{\sqrt{14}} \right)$
- $\vec a \cdot \vec b = -8$
- $\theta = \arccos\left(\frac{-8}{7\sqrt{6}}\right)$
- $\vec a \times \vec b = (-10, 7, 9)$
- $\text{Area} = \sqrt{230}$
- $A\vec a = (3, -4, 5)$
- $\det A = 1$

## Interpretation

The negative dot product indicates that the angle between vectors $\vec a$ and $\vec b$ is obtuse (greater than $90^\circ$). The matrix transformation has a determinant of $1$, which means the transformation preserves both the volume and the orientation of the vector space.