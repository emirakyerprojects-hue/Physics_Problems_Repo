# Task 04 – Motion of a particle in a uniform field

## Problem Statement

The following initial conditions are given for a particle:

* $m = 0.02 \ \mathrm{kg}$
* $q = 1 \ \mathrm{mC} = 10^{-3} \ \mathrm{C}$
* $\vec{E} = (30, 100) \ \mathrm{N/C}$
* $\vec{v}(0) = (20, 0) \ \mathrm{m/s}$
* $\vec{r}(0) = (0, 0) \ \mathrm{m}$

For them:
1. Write the equations of motion and solve them analytically.
2. Draw (describe mathematically) the motion trajectory.
3. Calculate the time to reach a vertical velocity of $50 \ \mathrm{m/s}$.
4. Calculate the kinetic energy after $t = 0.05 \ \mathrm{s}$.
5. Check the consistency with the energy balance.

## Theory

A charged particle in a uniform electric field $\vec{E}$ experiences a constant electrostatic force (Lorentz force for $\vec{B} = 0$):

$$
\vec{F} = q\vec{E}
$$

According to Newton's second law, this force produces a constant acceleration:

$$
\vec{a} = \frac{q}{m}\vec{E}
$$

Because the acceleration is constant, the equations of motion are given by standard kinematics:

$$
\vec{v}(t) = \vec{v}_0 + \vec{a}t
$$

$$
\vec{r}(t) = \vec{r}_0 + \vec{v}_0 t + \frac{1}{2} \vec{a} t^2
$$

The Work-Kinetic Energy Theorem states that the work $W$ done by the net force equals the change in kinetic energy $\Delta E_k$:

$$
W = \Delta E_k = E_k(t) - E_k(0)
$$

The work done by a constant force over a displacement $\Delta \vec{r}$ is:

$$
W = \vec{F} \cdot \Delta \vec{r} = F_x \Delta x + F_y \Delta y
$$

## Step-by-Step Solution

### 1. Equations of motion

First, determine the acceleration vector $\vec{a}$:

$$
\begin{align}
\vec{a} &= \frac{10^{-3} \ \mathrm{C}}{0.02 \ \mathrm{kg}} (30, 100) \ \mathrm{N/C} \\
        &= 0.05 (30, 100) \ \mathrm{m/s^2} \\
        &= (1.5, 5.0) \ \mathrm{m/s^2}
\end{align}
$$

Separating into $x$ and $y$ components, the initial velocities are $v_{0x} = 20 \ \mathrm{m/s}$ and $v_{0y} = 0 \ \mathrm{m/s}$. The initial positions are $x_0 = 0$ and $y_0 = 0$.

The velocity equations are:

$$
\begin{align}
v_x(t) &= 20 + 1.5t \\
v_y(t) &= 5.0t
\end{align}
$$

The position equations are:

$$
\begin{align}
x(t) &= 20t + \frac{1}{2}(1.5)t^2 = 20t + 0.75t^2 \\
y(t) &= \frac{1}{2}(5.0)t^2 = 2.5t^2
\end{align}
$$

### 2. Motion trajectory

The trajectory is described by the parametric equations $x(t)$ and $y(t)$ derived above. To find the explicit function $y(x)$, we isolate $t$ from the $y(t)$ equation (since it is simpler) or the $x(t)$ equation. 

From $y(t) = 2.5t^2$, we obtain:

$$
t = \sqrt{\frac{y}{2.5}}
$$

Substituting this into the $x(t)$ equation yields the trajectory curve $x(y)$:

$$
x(y) = 20 \sqrt{\frac{y}{2.5}} + 0.75 \left( \frac{y}{2.5} \right)
$$

This describes a parabolic curve in the $xy$-plane, opening outward due to the constant acceleration in both axes and the initial horizontal velocity. 

### 3. Time to reach a vertical velocity of $50 \ \mathrm{m/s}$

We set $v_y(t) = 50 \ \mathrm{m/s}$ and solve for $t$:

$$
5.0t = 50
$$

$$
t = 10 \ \mathrm{s}
$$

### 4. Kinetic energy after $t = 0.05 \ \mathrm{s}$

First, find the velocity components at $t = 0.05 \ \mathrm{s}$:

$$
\begin{align}
v_x(0.05) &= 20 + 1.5(0.05) = 20 + 0.075 = 20.075 \ \mathrm{m/s} \\
v_y(0.05) &= 5.0(0.05) = 0.25 \ \mathrm{m/s}
\end{align}
$$

The square of the speed $v^2$ is the sum of the squared components:

$$
\begin{align}
v^2 &= (20.075)^2 + (0.25)^2 \\
    &= 403.005625 + 0.0625 \\
    &= 403.068125 \ \mathrm{m^2/s^2}
\end{align}
$$

The kinetic energy is:

$$
\begin{align}
E_k(0.05) &= \frac{1}{2} m v^2 \\
          &= \frac{1}{2} (0.02) (403.068125) \\
          &= 0.01 (403.068125) \\
          &= 4.03068125 \ \mathrm{J}
\end{align}
$$

### 5. Consistency with the energy balance

The initial kinetic energy at $t=0$ was:

$$
E_k(0) = \frac{1}{2} (0.02) (20)^2 = 0.01 (400) = 4.0 \ \mathrm{J}
$$

The change in kinetic energy is:

$$
\Delta E_k = 4.03068125 \ \mathrm{J} - 4.0 \ \mathrm{J} = 0.03068125 \ \mathrm{J}
$$

Now, calculate the work done by the electric field. The force vector is:

$$
\begin{align}
\vec{F} &= q\vec{E} \\
        &= 10^{-3} (30, 100) \\
        &= (0.03, 0.1) \ \mathrm{N}
\end{align}
$$

The displacement at $t = 0.05 \ \mathrm{s}$ is calculated from the position equations:

$$
\begin{align}
x(0.05) &= 20(0.05) + 0.75(0.05)^2 = 1.0 + 0.75(0.0025) = 1.001875 \ \mathrm{m} \\
y(0.05) &= 2.5(0.05)^2 = 2.5(0.0025) = 0.00625 \ \mathrm{m}
\end{align}
$$

The work done is the dot product of force and displacement:

$$
\begin{align}
W &= F_x x + F_y y \\
  &= (0.03)(1.001875) + (0.1)(0.00625) \\
  &= 0.03005625 + 0.000625 \\
  &= 0.03068125 \ \mathrm{J}
\end{align}
$$

## Final Result

1. Kinematic equations: $x(t) = 20t + 0.75t^2$ and $y(t) = 2.5t^2$.
2. The trajectory is parabolic, defined mathematically by $x(y) = 20 \sqrt{\frac{y}{2.5}} + 0.3y$.
3. Time to reach $v_y = 50 \ \mathrm{m/s}$ is $10 \ \mathrm{s}$.
4. $E_k(0.05) \approx 4.0307 \ \mathrm{J}$.
5. $W = \Delta E_k = 0.03068125 \ \mathrm{J}$, which confirms energy conservation.

## Interpretation

The uniform electric field subjects the charged particle to a constant two-dimensional acceleration, strictly analogous to gravitational projectile motion but acting simultaneously along both the horizontal and vertical axes. Because the electric field does positive work on the particle, it constantly transfers energy to the system, accelerating the particle and continuously increasing its kinetic energy. The exact equivalence of the work integral and the change in kinetic energy verifies that electrostatic forces are conservative and obey the fundamental theorems of mechanics.