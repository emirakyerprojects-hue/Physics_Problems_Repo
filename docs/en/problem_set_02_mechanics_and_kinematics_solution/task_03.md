# Task 03 – Elimination of time and interpretation of acceleration

## Problem Statement

The path equation is given in parametric form:

$$
x(t) = 2t^2, \qquad y(t) = 3t^3
$$

Determine:
1. The path equation with the parameter $t$ eliminated.
2. The mathematical form of the trajectory to draw.
3. The vectors $\vec v(t)$ and $\vec a(t)$, and their magnitudes $|\vec v(t)|$ and $|\vec a(t)|$.
4. Whether the acceleration is constant.

## Theory

To find the Cartesian equation of the trajectory, the time parameter $t$ must be isolated in one equation and substituted into the other.

Kinematic vectors are obtained by progressive differentiation with respect to time. An acceleration is strictly constant only if both its magnitude and direction are independent of time.

## Step-by-Step Solution

### 1. Eliminating the parameter

From the equation for $x(t)$, assume $t \ge 0$ (since $x \ge 0$ for real $t$) and solve for $t$:

$$
t^2 = \frac{x}{2}
$$

$$
t = \left( \frac{x}{2} \right)^{1/2}
$$

Substitute this expression into the equation for $y(t)$:

$$
\begin{align}
y(x) &= 3 \left( \left( \frac{x}{2} \right)^{1/2} \right)^3 \\
     &= 3 \left( \frac{x}{2} \right)^{3/2}
\end{align}
$$

Squaring both sides yields an algebraic curve representation:

$$
y^2 = 9 \left( \frac{x}{2} \right)^3
$$

$$
y^2 = \frac{9}{8} x^3
$$

### 2. Trajectory drawing

The equation $y^2 = \frac{9}{8} x^3$ defines a semi-cubical parabola, also known as a cuspidal cubic. In the physical domain ($t \ge 0$), it represents a curve starting from the origin and rapidly growing in the first quadrant, curving upward as $y$ scales with $x^{1.5}$.

### 3. Velocity and Acceleration

**Velocity vector:**

$$
\begin{align}
\vec v(t) &= \left( \frac{dx}{dt}, \frac{dy}{dt} \right) \\
          &= (4t, 9t^2)
\end{align}
$$

**Velocity magnitude:**

$$
\begin{align}
|\vec v(t)| &= \sqrt{(4t)^2 + (9t^2)^2} \\
            &= \sqrt{16t^2 + 81t^4} \\
            &= t \sqrt{16 + 81t^2} \quad (\text{for } t \ge 0)
\end{align}
$$

**Acceleration vector:**

$$
\begin{align}
\vec a(t) &= \left( \frac{d v_x}{dt}, \frac{d v_y}{dt} \right) \\
          &= (4, 18t)
\end{align}
$$

**Acceleration magnitude:**

$$
\begin{align}
|\vec a(t)| &= \sqrt{4^2 + (18t)^2} \\
            &= \sqrt{16 + 324t^2} \\
            &= 2\sqrt{4 + 81t^2}
\end{align}
$$

### 4. Is the acceleration constant?

An acceleration vector is constant only if all its components are constant values independent of time.

Here, the $y$-component of acceleration is $a_y(t) = 18t$, which clearly depends on time $t$. Furthermore, the magnitude $|\vec a(t)|$ also depends on $t$. Therefore, the acceleration is not constant.

## Final Result

- Cartesian trajectory: $y = 3\left(\frac{x}{2}\right)^{3/2}$ or $y^2 = \frac{9}{8}x^3$
- $\vec v(t) = (4t, 9t^2)$
- $|\vec v(t)| = t \sqrt{16 + 81t^2}$
- $\vec a(t) = (4, 18t)$
- $|\vec a(t)| = 2\sqrt{4 + 81t^2}$
- The acceleration is not constant.

## Interpretation

The particle undergoes complex non-uniform motion. While the acceleration in the horizontal direction remains uniform ($4\ \text{m/s}^2$), the vertical acceleration linearly increases with time, leading to an increasingly steep trajectory in the $xy$-plane.