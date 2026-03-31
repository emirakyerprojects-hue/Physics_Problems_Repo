# Task 02 – Parametric trajectory, velocity, and acceleration

## Problem Statement

The parametric equation of a trajectory is given by:

$$
\vec r(t) = \bigl(t^2, \sin t, 5\bigr)
$$

Determine:
1. The velocity $\vec v(t) = \frac{d\vec r}{dt}$.
2. The acceleration $\vec a(t) = \frac{d^2 \vec r}{dt^2}$.
3. The magnitude of the velocity at $t=1$, $|\vec v(1)|$.
4. The dot product $\vec v \cdot \vec a$.
5. The cross product $\vec v \times \vec a$.

## Theory

The velocity vector is the first derivative of the position vector with respect to time. The acceleration vector is the second derivative of the position vector with respect to time (or the first derivative of the velocity vector).

The dot product of velocity and acceleration provides information about the tangential component of acceleration, indicating whether the particle is speeding up or slowing down. The cross product relates to the normal acceleration and the curvature of the trajectory.

## Step-by-Step Solution

### 1. Velocity

Differentiating each component of the position vector with respect to time:

$$
\begin{align}
\vec v(t) &= \frac{d}{dt} \bigl(t^2, \sin t, 5\bigr) \\
          &= (2t, \cos t, 0)
\end{align}
$$

### 2. Acceleration

Differentiating each component of the velocity vector with respect to time:

$$
\begin{align}
\vec a(t) &= \frac{d}{dt} (2t, \cos t, 0) \\
          &= (2, -\sin t, 0)
\end{align}
$$

### 3. Magnitude of velocity at $t=1$

Substitute $t=1$ into the velocity vector:

$$
\vec v(1) = (2(1), \cos(1), 0)
$$

$$
\vec v(1) = (2, \cos 1, 0)
$$

Compute the magnitude:

$$
\begin{align}
|\vec v(1)| &= \sqrt{2^2 + (\cos 1)^2 + 0^2} \\
            &= \sqrt{4 + \cos^2(1)}
\end{align}
$$

### 4. Dot product of velocity and acceleration

$$
\begin{align}
\vec v(t) \cdot \vec a(t) &= (2t)(2) + (\cos t)(-\sin t) + (0)(0) \\
                          &= 4t - \cos t \sin t
\end{align}
$$

### 5. Cross product of velocity and acceleration

$$
\begin{align}
\vec v(t) \times \vec a(t) &= \bigl((\cos t)(0) - (0)(-\sin t), (0)(2) - (2t)(0), (2t)(-\sin t) - (\cos t)(2)\bigr) \\
                           &= (0, 0, -2t \sin t - 2\cos t)
\end{align}
$$

## Final Result

- $\vec v(t) = (2t, \cos t, 0)$
- $\vec a(t) = (2, -\sin t, 0)$
- $|\vec v(1)| = \sqrt{4 + \cos^2(1)}$
- $\vec v \cdot \vec a = 4t - \cos t \sin t$
- $\vec v \times \vec a = (0, 0, -2t \sin t - 2\cos t)$

## Interpretation

The motion occurs in a plane parallel to the $xy$-plane because the $z$-component of position is constant ($z=5$), leading to zero $z$-components for both velocity and acceleration. The cross product $\vec v \times \vec a$ has only a $z$-component, confirming that the vector normal to the plane containing velocity and acceleration is perpendicular to the $xy$-plane.