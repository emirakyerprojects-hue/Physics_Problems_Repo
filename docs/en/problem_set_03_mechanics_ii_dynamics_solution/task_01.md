# Task 01 – Newton's second law (constant force)

## Problem Statement

A constant force acts on a body of mass $m = 2\ \mathrm{kg}$:

$$
\vec F = (6, 2)\ \mathrm{N}
$$

The body starts with an initial velocity $\vec v(0) = (1, -1)\ \mathrm{\frac{m}{s}}$ from the point $\vec r(0)=(0,0)\ \mathrm{m}$. 

Determine:
1. The acceleration vector $\vec a(t)$.
2. The velocity vector $\vec v(t)$.
3. The position vector $\vec r(t)$.
4. The characteristics of the trajectory.
5. The work done by the force at time $t=3\ \mathrm{s}$.
6. The consistency of the result with the work-energy theorem.

## Theory

Newton's second law relates the net force acting on a body to its mass and acceleration:

$$
\vec F = m \vec a
$$

Kinematic quantities are obtained by successive integration of the acceleration vector.

The mechanical work done by a constant force over a displacement $\Delta \vec r$ is defined as the dot product:

$$
W = \vec F \cdot \Delta \vec r
$$

The work-energy theorem states that the net work done on a body equals the change in its kinetic energy:

$$
W = \Delta K = K_f - K_i
$$

where kinetic energy is $K = \frac{1}{2} m |\vec v|^2$.

## Step-by-Step Solution

### 1. Acceleration vector

Using Newton's second law, solve for acceleration:

$$
\vec a = \frac{\vec F}{m}
$$

$$
\begin{align}
\vec a(t) &= \frac{(6, 2)}{2} \\
          &= (3, 1)\ \mathrm{\frac{m}{s^2}}
\end{align}
$$

### 2. Velocity vector

Integrate the acceleration vector with respect to time:

$$
\begin{align}
\vec v(t) &= \int \vec a \, dt \\
          &= (3t + C_1, t + C_2)
\end{align}
$$

Apply the initial condition $\vec v(0) = (1, -1)$:

$$
(C_1, C_2) = (1, -1)
$$

$$
\vec v(t) = (3t + 1, t - 1)\ \mathrm{\frac{m}{s}}
$$

### 3. Position vector

Integrate the velocity vector with respect to time:

$$
\begin{align}
\vec r(t) &= \int (3t + 1, t - 1) \, dt \\
          &= \left( \frac{3}{2}t^2 + t + C_3, \frac{1}{2}t^2 - t + C_4 \right)
\end{align}
$$

Apply the initial condition $\vec r(0) = (0, 0)$:

$$
(C_3, C_4) = (0, 0)
$$

$$
\vec r(t) = \left( \frac{3}{2}t^2 + t, \frac{1}{2}t^2 - t \right)\ \mathrm{m}
$$

### 4. Trajectory

The parametric equations of motion form a parabola in the $xy$-plane because both coordinates are quadratic functions of the same parameter $t$.

### 5. Work done by the force at $t=3$

Calculate the position vector at $t=3\ \mathrm{s}$:

$$
\begin{align}
\vec r(3) &= \left( \frac{3}{2}(3)^2 + 3, \frac{1}{2}(3)^2 - 3 \right) \\
          &= \left( \frac{27}{2} + 3, \frac{9}{2} - 3 \right) \\
          &= (13.5 + 3, 4.5 - 3) \\
          &= (16.5, 1.5)\ \mathrm{m}
\end{align}
$$

Since $\vec r(0) = (0,0)$, the displacement is $\Delta \vec r = (16.5, 1.5)$. Compute the work:

$$
\begin{align}
W &= \vec F \cdot \Delta \vec r \\
  &= (6)(16.5) + (2)(1.5) \\
  &= 99 + 3 \\
  &= 102\ \mathrm{J}
\end{align}
$$

### 6. Consistency with the work-energy theorem

Calculate the initial kinetic energy at $t=0$:

$$
|\vec v(0)|^2 = 1^2 + (-1)^2 = 2
$$

$$
\begin{align}
K_i &= \frac{1}{2} m |\vec v(0)|^2 \\
    &= \frac{1}{2} (2) (2) \\
    &= 2\ \mathrm{J}
\end{align}
$$

Calculate the final kinetic energy at $t=3$:

$$
\begin{align}
\vec v(3) &= (3(3) + 1, 3 - 1) \\
          &= (10, 2)\ \mathrm{\frac{m}{s}}
\end{align}
$$

$$
|\vec v(3)|^2 = 10^2 + 2^2 = 104
$$

$$
\begin{align}
K_f &= \frac{1}{2} m |\vec v(3)|^2 \\
    &= \frac{1}{2} (2) (104) \\
    &= 104\ \mathrm{J}
\end{align}
$$

Calculate the change in kinetic energy:

$$
\begin{align}
\Delta K &= K_f - K_i \\
         &= 104 - 2 \\
         &= 102\ \mathrm{J}
\end{align}
$$

## Final Result

- $\vec a(t) = (3, 1)$
- $\vec v(t) = (3t + 1, t - 1)$
- $\vec r(t) = \left( \frac{3}{2}t^2 + t, \frac{1}{2}t^2 - t \right)$
- $W = 102\ \mathrm{J}$
- The work-energy theorem holds exactly ($W = \Delta K = 102\ \mathrm{J}$).

## Interpretation

The constant force produces uniform acceleration, resulting in a parabolic trajectory in two dimensions. The equivalence of the calculated mechanical work and the change in kinetic energy verifies that no energy is lost to non-conservative forces, confirming the internal consistency of classical mechanics.