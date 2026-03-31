# Task 06 – Damped oscillator

## Problem Statement

The equation for a damped harmonic oscillator is:

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = 0
$$

Determine:
1. The derivation of the general solution.
2. The classification of cases: underdamped, critically damped, overdamped.
3. The method to solve the equation numerically using the 4th-order Runge-Kutta (RK4) algorithm.
4. The effect of the damping parameter $b$.
5. The setup for generating the $x(t)$ graph and the phase portrait, including an interactive HTML slider for $b$.

## Theory

Damping introduces a non-conservative force proportional to the velocity, dissipating the system's mechanical energy. 

The differential equation is a second-order linear homogeneous ODE with constant coefficients. Proposing an exponential solution $x(t) = e^{rt}$ transforms the differential equation into an algebraic characteristic equation. The nature of the roots of this polynomial dictates the dynamic behavior of the system.

## Step-by-Step Solution

### 1. General solution derivation

Divide the entire equation by the mass $m$:

$$
\frac{d^2 x}{dt^2} + \frac{b}{m} \frac{dx}{dt} + \frac{k}{m} x = 0
$$

Introduce defining parameters: the damping ratio $\gamma = \frac{b}{2m}$ and the undamped natural frequency $\omega_0^2 = \frac{k}{m}$.

$$
\ddot{x} + 2\gamma \dot{x} + \omega_0^2 x = 0
$$

Substitute the ansatz $x(t) = e^{rt}$:

$$
r^2 e^{rt} + 2\gamma r e^{rt} + \omega_0^2 e^{rt} = 0
$$

Since $e^{rt} \neq 0$, the characteristic equation is:

$$
r^2 + 2\gamma r + \omega_0^2 = 0
$$

Solve for $r$ using the quadratic formula:

$$
\begin{align}
r &= \frac{-2\gamma \pm \sqrt{4\gamma^2 - 4\omega_0^2}}{2} \\
  &= -\gamma \pm \sqrt{\gamma^2 - \omega_0^2}
\end{align}
$$

### 2. Classification of cases

The discriminant $\Delta' = \gamma^2 - \omega_0^2$ determines the three distinct physical regimes:

**Case I: Underdamped ($b^2 < 4mk \implies \gamma < \omega_0$)**
The discriminant is negative, yielding complex conjugate roots. Let $\omega_d = \sqrt{\omega_0^2 - \gamma^2}$ be the damped frequency.
$r = -\gamma \pm i\omega_d$

$$
x(t) = e^{-\gamma t} (A \cos(\omega_d t) + B \sin(\omega_d t))
$$
The system oscillates with an exponentially decaying amplitude.

**Case II: Critically damped ($b^2 = 4mk \implies \gamma = \omega_0$)**
The discriminant is exactly zero, yielding a single repeated real root $r = -\gamma$. To form the general solution, multiply the second term by $t$:

$$
x(t) = (A + Bt) e^{-\gamma t}
$$
The system returns to equilibrium as fast as possible without oscillating.

**Case III: Overdamped ($b^2 > 4mk \implies \gamma > \omega_0$)**
The discriminant is positive, yielding two distinct real negative roots $r_1$ and $r_2$.

$$
x(t) = A e^{r_1 t} + B e^{r_2 t}
$$
The system slowly creeps back toward equilibrium without oscillating.

### 3. Numerical solution (RK4)

To apply numerical integration, convert the second-order ODE into a system of two first-order ODEs:

Let $v = \dot{x}$.

$$
\frac{dx}{dt} = v
$$

$$
\frac{dv}{dt} = -\frac{b}{m}v - \frac{k}{m}x
$$

The RK4 algorithm updates the state $(x_n, v_n)$ to $(x_{n+1}, v_{n+1})$ by evaluating the derivatives at four distinct points (k1, k2, k3, k4) across the time step $\Delta t$, and computing a weighted average to achieve fourth-order accuracy.

### 4. Effect of parameter $b$

The parameter $b$ scales the velocity-dependent drag force. 
- As $b$ increases from 0, the amplitude of successive oscillations decreases more rapidly, and the oscillation frequency slightly lowers.
- At the critical threshold $b_c = 2\sqrt{mk}$, oscillation ceases completely.
- Further increasing $b$ merely slows down the return to equilibrium, acting like a thick, viscous syrup.

### 5. Visualization framework

An HTML/JS application requires:
- A state vector `[x, v]` updated iteratively in a `requestAnimationFrame` loop using the RK4 mathematical functions.
- Two HTML `<canvas>` elements:
  - **Graph 1 ($x$ vs $t$):** Plots the horizontal displacement against time, demonstrating the envelope decay.
  - **Graph 2 ($v$ vs $x$):** The Phase Portrait. For an underdamped system, it traces an inward-spiraling path toward the origin.
- An `<input type="range">` element mapped to the variable $b$, allowing real-time transition between the underdamped, critical, and overdamped regimes without halting the simulation.

## Final Result

- Characteristic roots: $r = -\frac{b}{2m} \pm \sqrt{\left(\frac{b}{2m}\right)^2 - \frac{k}{m}}$
- Underdamped: $x(t) = e^{-\gamma t} (C_1 \cos(\omega_d t) + C_2 \sin(\omega_d t))$
- Critically damped: $x(t) = (C_1 + C_2 t) e^{-\gamma t}$
- Overdamped: $x(t) = C_1 e^{r_1 t} + C_2 e^{r_2 t}$

## Interpretation

Damping provides the mathematical mechanism for energy dissipation. Critical damping is a highly desirable engineering target (e.g., in car shock absorbers and analog meter needles) because it ensures the fastest possible stabilization against disturbances without overshooting the target state.