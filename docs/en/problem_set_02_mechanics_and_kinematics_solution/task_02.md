# Task 02 – Projectile motion

## Problem Statement

A body moves in the Earth's gravitational field without air resistance, subjected to an initial velocity $v_0$ at an angle $\alpha$ relative to the horizontal. 

Determine:
1. The equations of motion in the horizontal and vertical directions.
2. The time of flight.
3. The maximum height.
4. The range.
5. The angle for which the range is maximum.
6. The mathematical setup required to animate the trajectory for varying $\alpha$.

## Theory

Projectile motion is a superposition of two independent one-dimensional motions: uniform linear motion in the horizontal direction (since horizontal acceleration is zero) and uniformly accelerated motion in the vertical direction (due to gravity, $g$).

The initial velocity vector is decomposed into components:

$$
v_{0x} = v_0 \cos\alpha
$$

$$
v_{0y} = v_0 \sin\alpha
$$

## Step-by-Step Solution

### 1. Equations of motion

The accelerations in the $x$ and $y$ directions are:

$$
a_x = 0
$$

$$
a_y = -g
$$

Integrating with respect to time yields the velocities:

$$
v_x(t) = v_0 \cos\alpha
$$

$$
v_y(t) = v_0 \sin\alpha - gt
$$

Integrating the velocities yields the position coordinates, assuming the origin $(0,0)$ as the starting point:

$$
x(t) = v_0 t \cos\alpha
$$

$$
y(t) = v_0 t \sin\alpha - \frac{1}{2} g t^2
$$

### 2. Time of flight

The time of flight $t_f$ is determined by finding the non-zero time when the vertical position $y(t)$ returns to zero:

$$
0 = v_0 t_f \sin\alpha - \frac{1}{2} g t_f^2
$$

Factoring out $t_f$:

$$
0 = t_f \left( v_0 \sin\alpha - \frac{1}{2} g t_f \right)
$$

Ignoring the trivial solution $t_f = 0$, solve for the remaining factor:

$$
t_f = \frac{2v_0 \sin\alpha}{g}
$$

### 3. Maximum height

The maximum height $H$ is reached when the vertical velocity becomes zero. Let $t_h$ be the time to reach maximum height:

$$
0 = v_0 \sin\alpha - g t_h
$$

$$
t_h = \frac{v_0 \sin\alpha}{g}
$$

Substitute $t_h$ into the vertical position equation to find $H$:

$$
\begin{align}
H &= y(t_h) \\
  &= v_0 \left( \frac{v_0 \sin\alpha}{g} \right) \sin\alpha - \frac{1}{2} g \left( \frac{v_0 \sin\alpha}{g} \right)^2 \\
  &= \frac{v_0^2 \sin^2\alpha}{g} - \frac{v_0^2 \sin^2\alpha}{2g} \\
  &= \frac{v_0^2 \sin^2\alpha}{2g}
\end{align}
$$

### 4. Range

The horizontal range $R$ is the horizontal distance traveled during the entire time of flight $t_f$:

$$
\begin{align}
R &= x(t_f) \\
  &= v_0 \left( \frac{2v_0 \sin\alpha}{g} \right) \cos\alpha \\
  &= \frac{v_0^2 (2 \sin\alpha \cos\alpha)}{g}
\end{align}
$$

Using the double-angle trigonometric identity $\sin(2\alpha) = 2\sin\alpha \cos\alpha$:

$$
R = \frac{v_0^2 \sin(2\alpha)}{g}
$$

### 5. Maximum range angle

To maximize the range for a given initial velocity, maximize the function $\sin(2\alpha)$. The maximum value of the sine function is $1$, which occurs when the argument is $\frac{\pi}{2}$:

$$
2\alpha = \frac{\pi}{2}
$$

$$
\alpha = \frac{\pi}{4} = 45^\circ
$$

Alternatively, take the derivative of $R$ with respect to $\alpha$ and set it to zero:

$$
\frac{dR}{d\alpha} = \frac{2v_0^2 \cos(2\alpha)}{g} = 0 \implies \cos(2\alpha) = 0 \implies 2\alpha = \frac{\pi}{2} \implies \alpha = 45^\circ
$$

### 6. Animation setup

To animate the trajectory, compute pairs of coordinates $(x_i, y_i)$ over discrete time steps $t_i \in [0, t_f]$. Overlaying curves for $\alpha \in \{30^\circ, 45^\circ, 60^\circ\}$ demonstrates that complementary angles (e.g., $30^\circ$ and $60^\circ$) yield the same range, but different maximum heights and flight times.

## Final Result

- $x(t) = v_0 t \cos\alpha$
- $y(t) = v_0 t \sin\alpha - \frac{1}{2}gt^2$
- $t_f = \frac{2v_0 \sin\alpha}{g}$
- $H = \frac{v_0^2 \sin^2\alpha}{2g}$
- $R = \frac{v_0^2 \sin(2\alpha)}{g}$
- Maximum range at $\alpha = 45^\circ$

## Interpretation

The independence of orthogonal motions implies that gravity affects only the vertical aspect of the flight. The parabolic trajectory dictates a geometric symmetry, explaining why it takes exactly half the time of flight to reach the maximum height.