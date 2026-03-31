# Task 10 – Numerical model of a dynamical system

## Problem Statement

Consider motion in a one-dimensional anharmonic potential:

$$
U(x) = \frac{k}{2}x^2 + \lambda x^4
$$

Determine:
1. The force $F(x)$.
2. The equation of motion.
3. The method to solve the equation numerically for selected parameters.
4. The effect of initial energy on the type of motion.
5. The setup for visualizing $x(t)$ and the phase portrait.

## Theory

The introduction of a quartic term ($\lambda x^4$) to the potential energy creates an anharmonic oscillator. If $\lambda > 0$, the restoring force grows stronger at large displacements than a linear spring (a "hard" spring). If $\lambda < 0$, the restoring force weakens at large displacements (a "soft" spring).

Because the resulting differential equation is non-linear, analytical solutions require complex elliptic integrals. Numerical integration is the standard approach to compute the trajectory.

## Step-by-Step Solution

### 1. Force

The conservative force is the negative derivative of the potential energy:

$$
\begin{align}
F(x) &= -\frac{dU}{dx} \\
     &= -\frac{d}{dx} \left( \frac{k}{2}x^2 + \lambda x^4 \right) \\
     &= -kx - 4\lambda x^3
\end{align}
$$

### 2. Equation of motion

Apply Newton's second law ($F = m\ddot{x}$):

$$
m\ddot{x} = -kx - 4\lambda x^3
$$

$$
\ddot{x} + \frac{k}{m}x + \frac{4\lambda}{m}x^3 = 0
$$

### 3. Numerical solution method

To solve this numerically, rewrite the second-order ODE as a system of two first-order ODEs:

$$
\frac{dx}{dt} = v
$$

$$
\frac{dv}{dt} = -\frac{k}{m}x - \frac{4\lambda}{m}x^3
$$

A robust algorithm like the 4th-order Runge-Kutta (RK4) or the symplectic Euler-Cromer method must be implemented. For Euler-Cromer:

$$
v_{i+1} = v_i + \left( -\frac{k}{m}x_i - \frac{4\lambda}{m}x_i^3 \right) \Delta t
$$

$$
x_{i+1} = x_i + v_{i+1} \Delta t
$$

### 4. Effect of initial energy

The initial total energy determines the amplitude of the oscillation.
- **For $\lambda > 0$:** As initial energy increases, the maximum displacement $x_{max}$ increases. The $x^3$ term dominates, causing the restoring force to increase drastically. This results in the oscillation frequency strictly increasing with higher energies (unlike a simple harmonic oscillator, where frequency is independent of amplitude).
- **For $\lambda < 0$:** As energy increases, the restoring force weakens compared to a linear spring. The frequency decreases. If the initial energy exceeds the local potential maxima at $x = \pm \sqrt{-k / (4\lambda)}$, the particle will escape the potential well entirely, leading to unbounded motion.

### 5. Visualization framework

- **Time series $x(t)$:** The plot of position versus time will resemble a sine wave for small energies. For large energies ($\lambda > 0$), the wave peaks become sharper and "triangular" because the particle spends less time at large amplitudes due to the overwhelming restoring force.
- **Phase portrait $(x, v)$:** The trajectory traces a closed contour for bounded motion. Instead of a perfect ellipse (as in $k$-only motion), the contour distorts into a "squarish" or rounded-rectangle shape for $\lambda > 0$.

## Final Result

- $F(x) = -kx - 4\lambda x^3$
- $m\ddot{x} = -kx - 4\lambda x^3$
- Frequency depends strictly on the initial energy (amplitude).
- The numerical approach requires a coupled system of first-order ODEs evaluated iteratively.

## Interpretation

Anharmonic potentials provide realistic models for molecular bonds and macroscopic springs stretched beyond their linear limits. The dependence of the period on the amplitude is a hallmark of non-linear dynamics, signifying a break from the simple scaling laws of purely quadratic potential wells.