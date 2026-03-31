# Task 07 – 2D motion with a given acceleration

## Problem Statement

Given is the constant acceleration vector and the initial conditions:

$$
\vec a = (2, -3)
$$

$$
\vec v(0) = (1, 0), \qquad \vec r(0) = (0, 0)
$$

Determine:
1. The velocity vector $\vec v(t)$.
2. The position vector $\vec r(t)$.
3. The method to draw the trajectory, velocity vector, and acceleration vector at selected moments in time.

## Theory

For a constant acceleration vector in two dimensions, the kinematic equations for velocity and position are obtained by direct integration with respect to time. The initial conditions determine the constants of integration.

$$
\vec v(t) = \int \vec a \, dt = \vec a t + \vec v(0)
$$

$$
\vec r(t) = \int \vec v(t) \, dt = \frac{1}{2} \vec a t^2 + \vec v(0) t + \vec r(0)
$$

## Step-by-Step Solution

### 1. Velocity vector

Integrate the constant acceleration vector:

$$
\begin{align}
\vec v(t) &= \int (2, -3) \, dt \\
          &= (2t + C_1, -3t + C_2)
\end{align}
$$

Apply the initial velocity condition $\vec v(0) = (1, 0)$:

$$
(2(0) + C_1, -3(0) + C_2) = (1, 0)
$$

$$
(C_1, C_2) = (1, 0)
$$

Substitute the constants back into the velocity equation:

$$
\vec v(t) = (2t + 1, -3t)
$$

### 2. Position vector

Integrate the velocity vector to find the position:

$$
\begin{align}
\vec r(t) &= \int (2t + 1, -3t) \, dt \\
          &= \left( t^2 + t + C_3, -\frac{3}{2}t^2 + C_4 \right)
\end{align}
$$

Apply the initial position condition $\vec r(0) = (0, 0)$:

$$
\left( 0^2 + 0 + C_3, -\frac{3}{2}(0)^2 + C_4 \right) = (0, 0)
$$

$$
(C_3, C_4) = (0, 0)
$$

Substitute the constants back into the position equation:

$$
\vec r(t) = \left( t^2 + t, -\frac{3}{2}t^2 \right)
$$

### 3. Visualization

To graph the motion mathematically:
- **Trajectory:** Plot the parametric curve $(x(t), y(t)) = (t^2 + t, -1.5t^2)$ for $t \ge 0$. This represents a parabolic path opening downward and to the right.
- **Velocity vector:** At any selected point $\vec r(t_1)$, draw an arrow starting at $\vec r(t_1)$ with components $(2t_1 + 1, -3t_1)$. It will be tangent to the trajectory.
- **Acceleration vector:** At the same point, draw an arrow with components $(2, -3)$. This vector remains constant in magnitude and direction regardless of the chosen time $t_1$.

## Final Result

- $\vec v(t) = (2t + 1, -3t)$
- $\vec r(t) = \left( t^2 + t, -\frac{3}{2}t^2 \right)$

## Interpretation

The motion represents a standard parabolic trajectory under uniform acceleration, analogous to projectile motion but oriented differently. The positive horizontal acceleration causes the horizontal velocity to continuously increase, while the negative vertical acceleration causes a continuous downward curve.