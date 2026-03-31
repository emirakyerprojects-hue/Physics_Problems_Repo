# Task 04 – Conservation of energy

## Problem Statement

A body falls from a height $h$ without air resistance.

Determine:
1. The total energy equation $E(h) = T(h) + U(h)$.
2. The velocity as a function of vertical position $v(y)$.
3. The comparison between the energy-derived solution and the solution obtained via Newton's second law.
4. The height at which the kinetic energy accounts for 75% of the total energy.

## Theory

The principle of conservation of mechanical energy states that in the absence of non-conservative forces (like air resistance), the total mechanical energy $E$ of an isolated system remains constant.

Total mechanical energy is the sum of kinetic energy $T$ and potential energy $U$:

$$
E = T + U = \frac{1}{2}mv^2 + mgy = \text{const}
$$

Newton's second law for a body in free fall relates the constant gravitational force to a constant acceleration, leading to standard kinematic equations for uniformly accelerated motion.

## Step-by-Step Solution

### 1. Total energy equation

Set the reference point for potential energy at the ground ($y = 0$, so $U(0) = 0$). 
At the initial height $h$, the body is released from rest ($v = 0$).

The initial total energy is:

$$
\begin{align}
E(h) &= T(h) + U(h) \\
     &= \frac{1}{2}m(0)^2 + mgh \\
     &= mgh
\end{align}
$$

At an arbitrary height $y$ during the fall, the total energy is:

$$
E(y) = \frac{1}{2}mv^2 + mgy
$$

By conservation of energy, $E(y) = E(h)$:

$$
\frac{1}{2}mv^2 + mgy = mgh
$$

### 2. Velocity as a function of height

Solve the energy equation for the velocity $v$:

$$
\frac{1}{2}mv^2 = mgh - mgy
$$

$$
\frac{1}{2}v^2 = g(h - y)
$$

$$
v(y) = \sqrt{2g(h - y)}
$$

### 3. Comparison with Newton's second law

From Newton's second law, the only force is gravity, pointing downwards:

$$
F_y = -mg
$$

$$
ma_y = -mg \implies a_y = -g
$$

Using the time-independent kinematic equation relating velocity, acceleration, and displacement:

$$
v_f^2 = v_i^2 + 2a\Delta y
$$

Substitute $v_i = 0$, $a = -g$, and $\Delta y = y - h$:

$$
v^2 = 0 + 2(-g)(y - h)
$$

$$
v^2 = 2g(h - y)
$$

$$
v(y) = \sqrt{2g(h - y)}
$$

The solution derived from kinematics exactly matches the solution derived from energy conservation.

### 4. Height where kinetic energy is 75% of total energy

The condition is given as:

$$
T = 0.75 E
$$

Since $E = T + U$, it follows that the potential energy must account for the remaining 25% of the total energy:

$$
U = 0.25 E
$$

Substitute the expressions for $U$ and $E$:

$$
mgy = 0.25 mgh
$$

Divide by $mg$:

$$
y = 0.25 h
$$

$$
y = \frac{h}{4}
$$

## Final Result

- $E = \frac{1}{2}mv^2 + mgy = mgh$
- $v(y) = \sqrt{2g(h - y)}$
- The kinematic derivation perfectly reproduces the energy derivation.
- The kinetic energy is 75% of the total energy at the height $y = \frac{h}{4}$.

## Interpretation

Energy conservation provides a direct scalar method for determining the speed of a particle solely based on its spatial position, bypassing the need to compute vectors or integrate over time. Because the object loses potential energy linearly with falling distance, its kinetic energy increases linearly with fallen distance, meaning 75% kinetic energy corresponds exactly to falling 75% of the way down.