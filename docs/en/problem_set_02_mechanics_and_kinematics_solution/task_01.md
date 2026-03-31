# Task 01 – Uniform and uniformly accelerated motion

## Problem Statement

The equation of motion is given by:

$$
x(t) = x_0 + v_0 t + \frac{1}{2} a t^2
$$

Determine:
1. The velocity $v(t)$ and acceleration $a(t)$.
2. For the specific parameters $x_0 = 0$, $v_0 = 5\ \text{m/s}$, and $a = -2\ \text{m/s}^2$:
   - The stopping time.
   - The maximum velocity depending on the time and the sign of the acceleration.
   - The maximum displacement.
3. The mathematical framework required to visualize $x(t)$, $v(t)$, and $a(t)$.

## Theory

Kinematic relationships for one-dimensional continuous motion dictate that velocity is the first time derivative of position, and acceleration is the first time derivative of velocity (or the second time derivative of position). 

The stopping time is defined as the instance when the instantaneous velocity becomes zero. 

The maximum displacement in a given direction occurs when the velocity changes sign, which mathematically corresponds to a local extremum of the position function.

## Step-by-Step Solution

### 1. Velocity and Acceleration

Differentiate the position function with respect to time to find the velocity:

$$
\begin{align}
v(t) &= \frac{d}{dt} \left( x_0 + v_0 t + \frac{1}{2} a t^2 \right) \\
     &= v_0 + at
\end{align}
$$

Differentiate the velocity function with respect to time to find the acceleration:

$$
\begin{align}
a(t) &= \frac{d}{dt} \left( v_0 + at \right) \\
     &= a
\end{align}
$$

The acceleration is constant.

### 2. Specific Parameters Analysis

Substitute the given values ($x_0 = 0$, $v_0 = 5$, $a = -2$) into the general equations:

$$
x(t) = 5t - t^2
$$

$$
v(t) = 5 - 2t
$$

**Stopping time:**
Set the velocity to zero and solve for $t$:

$$
0 = 5 - 2t
$$

$$
2t = 5
$$

$$
t = 2.5\ \text{s}
$$

**Maximum velocity:**
Since the acceleration is negative ($a = -2\ \text{m/s}^2$), the velocity is a strictly decreasing linear function for $t \ge 0$. Therefore, the maximum velocity occurs at the initial time $t = 0$.

$$
v_{max} = v(0) = 5\ \text{m/s}
$$

If the acceleration were positive, the velocity would increase indefinitely over time, meaning a maximum would only exist if the time interval were bounded.

**Maximum displacement:**
The maximum displacement in the positive $x$-direction occurs at the stopping time $t = 2.5\ \text{s}$, immediately before the object reverses its direction of motion. Substitute this time into the position equation:

$$
\begin{align}
x_{max} &= x(2.5) \\
        &= 5(2.5) - (2.5)^2 \\
        &= 12.5 - 6.25 \\
        &= 6.25\ \text{m}
\end{align}
$$

### 3. Visualization Framework

To visualize the kinematic quantities programmatically, plot the following functions for $t \ge 0$:
- Position: A downward-opening parabola passing through the origin with a vertex at $(2.5, 6.25)$.
- Velocity: A straight line with a negative slope, intersecting the $v$-axis at $5$ and the $t$-axis at $2.5$.
- Acceleration: A horizontal line intersecting the $a$-axis at $-2$.

## Final Result

- $v(t) = v_0 + at$
- $a(t) = a$
- Stopping time: $t = 2.5\ \text{s}$
- Maximum velocity: $v_{max} = 5\ \text{m/s}$ (at $t=0$)
- Maximum displacement: $x_{max} = 6.25\ \text{m}$

## Interpretation

The specified parameters describe an object undergoing constant deceleration. The positive initial velocity and negative acceleration imply that the object moves forward while slowing down, momentarily stops at $t = 2.5\ \text{s}$, and subsequently accelerates in the negative direction. The parabolic position curve confirms that the forward progress is bounded.