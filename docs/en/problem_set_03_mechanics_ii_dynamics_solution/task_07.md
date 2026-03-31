# Task 07 – Vertical throw with drag

## Problem Statement

The equation of motion for a vertical throw with linear drag is given by:

$$
m\frac{dv}{dt} = -mg - kv
$$

Initial conditions: $v(0) = v_0$, $x(0) = 0$.

Determine:
1. The solution to the equation of motion for $v(t)$ and $x(t)$.
2. The maximum height $H_{max}$.
3. A comparison with the case without drag.
4. The framework for a numerical simulation.
5. A comparison between the analytical and numerical solutions.

## Theory

A body thrown vertically upwards in a resisting medium experiences a downward gravitational force and a drag force that opposes its instantaneous velocity. 

The equation of motion is a first-order linear ordinary differential equation for velocity. The maximum height is achieved when the instantaneous velocity reaches zero. In the absence of drag ($k = 0$), the system reduces to uniformly accelerated motion.

## Step-by-Step Solution

### 1. Analytical Solution

Rearrange the equation of motion to separate the variables:

$$
m \frac{dv}{dt} = -k \left( \frac{mg}{k} + v \right)
$$

$$
\frac{dv}{v + \frac{mg}{k}} = -\frac{k}{m} \, dt
$$

Integrate both sides:

$$
\int \frac{1}{v + \frac{mg}{k}} \, dv = \int -\frac{k}{m} \, dt
$$

$$
\ln\left| v + \frac{mg}{k} \right| = -\frac{k}{m}t + C_1
$$

Exponentiate to solve for $v$:

$$
v(t) + \frac{mg}{k} = C_2 e^{-\frac{k}{m}t}
$$

Apply the initial condition $v(0) = v_0$:

$$
v_0 + \frac{mg}{k} = C_2
$$

The velocity function is:

$$
v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}
$$

Integrate the velocity to find the position $x(t)$:

$$
\begin{align}
x(t) &= \int \left[ \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k} \right] dt \\
     &= -\frac{m}{k} \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}t + C_3
\end{align}
$$

Apply the initial condition $x(0) = 0$:

$$
0 = -\frac{m}{k} \left( v_0 + \frac{mg}{k} \right) + C_3
$$

$$
C_3 = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right)
$$

The position function is:

$$
x(t) = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mg}{k}t
$$

### 2. Maximum height

The maximum height occurs at time $t_m$ when $v(t_m) = 0$:

$$
0 = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t_m} - \frac{mg}{k}
$$

$$
e^{\frac{k}{m}t_m} = \frac{k v_0}{mg} + 1
$$

$$
t_m = \frac{m}{k} \ln\left( 1 + \frac{k v_0}{mg} \right)
$$

Substitute $t_m$ into the position equation to find $H_{max}$:

$$
\begin{align}
H_{max} &= \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - \frac{1}{1 + \frac{k v_0}{mg}} \right) - \frac{mg}{k} \left( \frac{m}{k} \ln\left( 1 + \frac{k v_0}{mg} \right) \right) \\
        &= \frac{m}{k} \left( \frac{mg + k v_0}{k} \right) \left( \frac{k v_0}{mg + k v_0} \right) - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right) \\
        &= \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right)
\end{align}
$$

### 3. Comparison with the case without drag

Without drag ($k = 0$), the maximum height is derived purely from kinematics:

$$
H_0 = \frac{v_0^2}{2g}
$$

The Taylor expansion of the logarithmic term in $H_{max}$ for small $k$ yields $H_{max} \approx \frac{v_0^2}{2g} - \frac{k v_0^3}{3 m g^2}$. Thus, $H_{max} < H_0$, demonstrating that the drag force dissipates kinetic energy, resulting in a lower peak altitude.

### 4. Numerical simulation framework

To solve the system numerically, apply the Euler method or a higher-order Runge-Kutta method. Discretize time into steps $\Delta t$.

$$
v_{i+1} = v_i - \left( g + \frac{k}{m} v_i \right) \Delta t
$$

$$
x_{i+1} = x_i + v_i \Delta t
$$

### 5. Analytical vs. Numerical comparison

The analytical solution provides the exact continuous trajectory. The numerical solution introduces a truncation error dependent on $\Delta t$. By plotting both $x(t)$ functions simultaneously, the numerical approximation will slightly diverge from the exact curve, with the error accumulating over time. Reducing $\Delta t$ forces the numerical trace to converge toward the exact analytical locus.

## Final Result

- $v(t) = \left( v_0 + \frac{mg}{k} \right) e^{-\frac{k}{m}t} - \frac{mg}{k}$
- $x(t) = \frac{m}{k} \left( v_0 + \frac{mg}{k} \right) \left( 1 - e^{-\frac{k}{m}t} \right) - \frac{mg}{k}t$
- $H_{max} = \frac{m v_0}{k} - \frac{m^2 g}{k^2} \ln\left( 1 + \frac{k v_0}{mg} \right)$
- Drag decreases the maximum height compared to the $k=0$ case.

## Interpretation

The presence of a velocity-dependent drag force breaks the symmetry of the parabolic trajectory. The ascent time is strictly shorter than the descent time, and the body returns to the initial position with a terminal velocity lower in magnitude than the initial throw velocity.