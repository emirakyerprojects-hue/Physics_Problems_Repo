# Task 07 – Forced oscillator and resonance

## Problem Statement

The equation of motion for a driven, damped harmonic oscillator is given by:

$$
m \frac{d^2 x}{dt^2} + b \frac{dx}{dt} + k x = F_0 \cos(\Omega t)
$$

Determine:
1. The analytical solution, finding the steady-state amplitude $A(\Omega)$ and phase shift $\phi(\Omega)$.
2. The framework for solving the equation numerically.
3. The behavior of the steady-state amplitude as a function of the driving frequency $\Omega$.
4. The generation of the resonance curve.
5. The behavior of the phase shift.
6. The physical interpretation of resonance, including an interactive HTML setup.

## Theory

A forced oscillator experiences an external, time-varying driving force in addition to restoring and damping forces. The general solution consists of a transient part (which decays over time due to damping) and a steady-state part (which persists at the driving frequency $\Omega$).

The steady-state solution can be assumed to have the form:

$$
x_p(t) = A \cos(\Omega t - \phi)
$$

where $A$ is the amplitude of the forced response and $\phi$ is the phase lag of the displacement relative to the driving force.

## Step-by-Step Solution

### 1. Analytical solution for amplitude and phase

Substitute the steady-state ansatz $x_p(t) = A \cos(\Omega t - \phi)$ into the differential equation. 
The derivatives are:

$$
\dot{x}_p = -A \Omega \sin(\Omega t - \phi)
$$

$$
\ddot{x}_p = -A \Omega^2 \cos(\Omega t - \phi)
$$

Substitute into the equation of motion:

$$
-m A \Omega^2 \cos(\Omega t - \phi) - b A \Omega \sin(\Omega t - \phi) + k A \cos(\Omega t - \phi) = F_0 \cos(\Omega t)
$$

Group the terms using trigonometric addition formulas. A more elegant approach uses complex exponentials, where the driving force is $\tilde{F} = F_0 e^{i\Omega t}$ and the response is $\tilde{x} = \tilde{A} e^{i\Omega t}$, with $\tilde{A} = A e^{-i\phi}$.

$$
(-m \Omega^2 + i b \Omega + k) \tilde{A} e^{i\Omega t} = F_0 e^{i\Omega t}
$$

Solve for the complex amplitude $\tilde{A}$:

$$
\tilde{A} = \frac{F_0}{(k - m\Omega^2) + i(b\Omega)}
$$

The physical amplitude $A$ is the magnitude of $\tilde{A}$:

$$
\begin{align}
A(\Omega) &= |\tilde{A}| \\
          &= \frac{F_0}{\sqrt{(k - m\Omega^2)^2 + (b\Omega)^2}}
\end{align}
$$

Dividing numerator and denominator by $m$ and introducing $\omega_0^2 = \frac{k}{m}$ and $\gamma = \frac{b}{2m}$:

$$
A(\Omega) = \frac{F_0 / m}{\sqrt{(\omega_0^2 - \Omega^2)^2 + (2\gamma\Omega)^2}}
$$

The phase angle $\phi$ is the argument of the complex denominator:

$$
\tan\phi = \frac{b\Omega}{k - m\Omega^2} = \frac{2\gamma\Omega}{\omega_0^2 - \Omega^2}
$$

### 2. Numerical solution framework

Rewrite as a system of first-order ODEs for RK4 integration:

$$
\frac{dx}{dt} = v
$$

$$
\frac{dv}{dt} = \frac{F_0}{m} \cos(\Omega t) - \frac{b}{m} v - \frac{k}{m} x
$$

### 3. Steady-state amplitude vs $\Omega$

The amplitude $A(\Omega)$ strongly depends on the driving frequency.
- As $\Omega \to 0$, $A \to \frac{F_0}{k}$ (static displacement).
- As $\Omega \to \infty$, $A \to 0$ (inertia dominates).
- When $\Omega \approx \omega_0$, the denominator reaches a minimum, causing a sharp peak in amplitude.

### 4. Resonance curve generation

The resonance curve plots $A$ versus $\Omega$. To find the exact resonant frequency $\Omega_r$ where amplitude is maximum, minimize the term under the square root with respect to $\Omega^2$:

$$
\frac{d}{d(\Omega^2)} \left[ (\omega_0^2 - \Omega^2)^2 + 4\gamma^2\Omega^2 \right] = 0
$$

$$
-2(\omega_0^2 - \Omega^2) + 4\gamma^2 = 0
$$

$$
\Omega_r = \sqrt{\omega_0^2 - 2\gamma^2}
$$

For lightly damped systems ($\gamma \ll \omega_0$), $\Omega_r \approx \omega_0$.

### 5. Phase shift investigation

The phase lag $\phi(\Omega)$ describes how the system's movement tracks the force:
- For $\Omega \ll \omega_0$, $\tan\phi \to 0 \implies \phi \approx 0$ (in phase).
- At exact resonance $\Omega = \omega_0$, the denominator is zero, so $\tan\phi \to \infty \implies \phi = \pi/2$ (velocity is in phase with force).
- For $\Omega \gg \omega_0$, $\tan\phi \to -0 \implies \phi \approx \pi$ (completely out of phase).

## Final Result

- $A(\Omega) = \frac{F_0}{\sqrt{(k - m\Omega^2)^2 + (b\Omega)^2}}$
- $\tan\phi = \frac{b\Omega}{k - m\Omega^2}$
- Resonance frequency: $\Omega_r = \sqrt{\omega_0^2 - \frac{b^2}{2m^2}}$

## Interpretation

Resonance occurs when the external driving force precisely matches the natural rhythms of the system, efficiently pumping energy into the oscillator. The damping coefficient $b$ prevents the amplitude from reaching infinity and shifts the peak slightly below the undamped natural frequency. An interactive HTML simulation allowing dynamic tuning of $\Omega$ effectively demonstrates the transition from low-amplitude tracking to resonant amplification and finally to high-frequency decoupling.