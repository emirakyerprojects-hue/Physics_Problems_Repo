# Task 02 – Energy of a harmonic oscillator

## Problem Statement

A system with the following initial parameters is given:
- $m = 1\ \mathrm{kg}$
- $k = 100\ \mathrm{N/m}$
- $x(0) = 2\ \mathrm{m}$
- $v(0) = 1\ \mathrm{m/s}$

Determine:
1. The natural frequency.
2. The total energy of the system.
3. The displacement for which the kinetic energy accounts for 50% of the total energy.

## Theory

The natural angular frequency of a mass-spring system depends solely on its mass and the spring constant.

Total mechanical energy $E$ in an undamped harmonic oscillator is conserved and is the sum of the instantaneous kinetic energy $K$ and potential energy $U$.

$$
E = K + U = \frac{1}{2}mv^2 + \frac{1}{2}kx^2 = \text{const}
$$

## Step-by-Step Solution

### 1. Natural frequency

The natural angular frequency $\omega_0$ is given by:

$$
\begin{align}
\omega_0 &= \sqrt{\frac{k}{m}} \\
         &= \sqrt{\frac{100}{1}} \\
         &= 10\ \mathrm{rad/s}
\end{align}
$$

The natural frequency $f_0$ in Hertz is:

$$
\begin{align}
f_0 &= \frac{\omega_0}{2\pi} \\
    &= \frac{10}{2\pi} \\
    &= \frac{5}{\pi}\ \mathrm{Hz} \approx 1.59\ \mathrm{Hz}
\end{align}
$$

### 2. Total energy of the system

Using the initial conditions to find the conserved total energy:

$$
\begin{align}
E &= \frac{1}{2}m(v(0))^2 + \frac{1}{2}k(x(0))^2 \\
  &= \frac{1}{2}(1)(1)^2 + \frac{1}{2}(100)(2)^2 \\
  &= 0.5 + \frac{1}{2}(100)(4) \\
  &= 0.5 + 200 \\
  &= 200.5\ \mathrm{J}
\end{align}
$$

### 3. Displacement for 50% kinetic energy

If the kinetic energy $K$ is 50% of the total energy $E$, then by conservation of energy ($E = K + U$), the potential energy $U$ must also account for the remaining 50% of the total energy:

$$
U = 0.5 E
$$

Substitute the expression for potential energy:

$$
\frac{1}{2}kx^2 = 0.5 E
$$

Solve for $x^2$:

$$
\begin{align}
x^2 &= \frac{E}{k} \\
    &= \frac{200.5}{100} \\
    &= 2.005\ \mathrm{m^2}
\end{align}
$$

Take the square root to find the displacement $x$:

$$
x = \pm \sqrt{2.005}\ \mathrm{m} \approx \pm 1.416\ \mathrm{m}
$$

## Final Result

- $\omega_0 = 10\ \mathrm{rad/s}$ (or $f_0 = 5/\pi\ \mathrm{Hz}$)
- $E = 200.5\ \mathrm{J}$
- $x = \pm \sqrt{2.005}\ \mathrm{m} \approx \pm 1.416\ \mathrm{m}$

## Interpretation

The total mechanical energy is determined entirely by the state of the system at any single instant and remains constant thereafter. The point where kinetic and potential energies are equal does not occur at half the maximum displacement ($A/2$), but rather at $x = A/\sqrt{2}$, because the potential energy scales quadratically with displacement, not linearly.