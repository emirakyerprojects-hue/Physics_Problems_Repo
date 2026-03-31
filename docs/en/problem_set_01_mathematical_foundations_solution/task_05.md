# Task 05 – Trajectory curvature and normal acceleration

## Problem Statement

For an ellipse described by $x = a\cos t, \quad y = b\sin t$:
1. Determine the velocity vector $\vec v(t)$ and acceleration vector $\vec a(t)$.
2. Determine the unit tangent vector $\hat T(t)$.
3. Decompose the acceleration into tangential and normal components and determine the magnitude of the normal acceleration $a_n(t)$.
4. Determine the radius of curvature $R$ at $t=0$.
5. Compare the result with the case of a circle ($a=b$).
6. Provide physical interpretations for curvature, normal acceleration, and direction of motion.

## Theory

The unit tangent vector points in the direction of the velocity:

$$
\hat T(t) = \frac{\vec v(t)}{|\vec v(t)|}
$$

Acceleration can be decomposed into a component parallel to the velocity (tangential, $a_t$) and a component perpendicular to the velocity (normal, $a_n$). The tangential component changes the speed, while the normal component changes the direction. 

The normal acceleration magnitude is computed using the cross product (for 2D vectors extending into 3D as $z=0$):

$$
a_n = \frac{|\vec v \times \vec a|}{|\vec v|}
$$

The radius of curvature $R$ is strictly related to normal acceleration and speed:

$$
a_n = \frac{v^2}{R} \implies R = \frac{v^2}{a_n}
$$

## Step-by-Step Solution

### 1. Velocity and Acceleration

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

### 2. Unit Tangent Vector

The speed is the magnitude of velocity:

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

The unit tangent vector is:

$$
\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)
$$

### 3. Normal Acceleration

To find $a_n$, compute the cross product $\vec v \times \vec a$ (treating them as 3D vectors with zero $z$-component):

$$
\begin{align}
\vec v \times \vec a &= (-a\sin t)(-b\sin t) - (b\cos t)(-a\cos t) \\
                     &= ab\sin^2 t + ab\cos^2 t \\
                     &= ab(\sin^2 t + \cos^2 t) \\
                     &= ab
\end{align}
$$

The magnitude of the normal acceleration is:

$$
a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}
$$

### 4. Radius of Curvature at $t=0$

First, formulate the general radius of curvature:

$$
\begin{align}
R(t) &= \frac{|\vec v(t)|^2}{a_n(t)} \\
     &= \frac{a^2\sin^2 t + b^2\cos^2 t}{\frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}} \\
     &= \frac{(a^2\sin^2 t + b^2\cos^2 t)^{3/2}}{ab}
\end{align}
$$

Evaluate at $t=0$:

$$
\begin{align}
R(0) &= \frac{(a^2\sin^2(0) + b^2\cos^2(0))^{3/2}}{ab} \\
     &= \frac{(b^2)^{3/2}}{ab} \\
     &= \frac{b^3}{ab} \\
     &= \frac{b^2}{a}
\end{align}
$$

### 5. Comparison with a Circle

For a circle, $a = b$. Substituting this into the radius of curvature formula at $t=0$:

$$
\begin{align}
R(0) &= \frac{a^2}{a} \\
     &= a
\end{align}
$$

This matches the expected behavior, as the radius of curvature for a circle is constant and equal to its geometric radius.

## Final Result

- $\hat T(t) = \frac{1}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}} (-a\sin t, b\cos t)$
- $a_n(t) = \frac{ab}{\sqrt{a^2\sin^2 t + b^2\cos^2 t}}$
- $R(0) = \frac{b^2}{a}$

## Interpretation

**Does greater trajectory curvature imply greater normal acceleration?**
Yes. Curvature $\kappa$ is defined as $1/R$. Because $a_n = v^2 \kappa$, a larger curvature directly increases the normal acceleration required to maintain that tight turn, assuming speed $v$ is constant.

**Where on the ellipse is the trajectory more "curved"?**
Curvature is maximized where $R$ is minimized. If $a > b$ (major axis along $x$), $R(0) = b^2/a$ is smaller than $R(\pi/2) = a^2/b$. Therefore, the trajectory is more "curved" at the vertices of the major axis.

**Why does normal acceleration act as the cause of change in direction?**
By definition, normal acceleration is orthogonal to the velocity vector ($\vec a_n \cdot \vec v = 0$). In terms of energy, a force purely perpendicular to motion performs zero work ($dW = \vec F \cdot d\vec r = 0$), meaning it cannot change the kinetic energy (or speed) of the particle. Its sole effect is to continuously rotate the velocity vector.