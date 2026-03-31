# Task 08 – Harmonic oscillator (formal dynamics)

## Problem Statement

The formal dynamics of a harmonic oscillator are governed by:

$$
m\ddot{x} + kx = 0
$$

Determine:
1. The solution to the equation.
2. The natural frequency $\omega_0$.
3. The total energy as a function of time $E(t)$.
4. The mathematical proof that energy is conserved.
5. The interpretation of the motion in phase space.

## Theory

A simple harmonic oscillator is a fundamental mechanical system subjected exclusively to a linear restoring force.

The differential equation is a second-order linear homogeneous equation with constant coefficients. 

The phase space of a one-dimensional system is a two-dimensional plot of momentum (or velocity) versus position $(x, v)$.

## Step-by-Step Solution

### 1. Solution to the equation

Divide the equation by $m$:

$$
\ddot{x} + \frac{k}{m} x = 0
$$

Let $\omega_0^2 = \frac{k}{m}$. The characteristic equation is $r^2 + \omega_0^2 = 0$, yielding purely imaginary roots $r = \pm i\omega_0$. The general solution is:

$$
x(t) = A \cos(\omega_0 t + \phi)
$$

where $A$ is the amplitude and $\phi$ is the phase constant, determined by initial conditions.

### 2. Natural frequency

The natural angular frequency $\omega_0$ is the parameter defining the periodicity of the system:

$$
\omega_0 = \sqrt{\frac{k}{m}}
$$

### 3. Energy as a function of time

Total mechanical energy is the sum of kinetic ($T$) and potential ($U$) energy:

$$
E(t) = \frac{1}{2}m \dot{x}^2(t) + \frac{1}{2}k x^2(t)
$$

Differentiate the position function to obtain velocity:

$$
\dot{x}(t) = -A \omega_0 \sin(\omega_0 t + \phi)
$$

Substitute $x(t)$ and $\dot{x}(t)$ into the energy equation:

$$
\begin{align}
E(t) &= \frac{1}{2}m \left( -A \omega_0 \sin(\omega_0 t + \phi) \right)^2 + \frac{1}{2}k \left( A \cos(\omega_0 t + \phi) \right)^2 \\
     &= \frac{1}{2}m A^2 \omega_0^2 \sin^2(\omega_0 t + \phi) + \frac{1}{2}k A^2 \cos^2(\omega_0 t + \phi)
\end{align}
$$

### 4. Proof of energy conservation

Substitute $\omega_0^2 = \frac{k}{m}$ into the kinetic energy term:

$$
\frac{1}{2}m A^2 \left( \frac{k}{m} \right) \sin^2(\omega_0 t + \phi) = \frac{1}{2}k A^2 \sin^2(\omega_0 t + \phi)
$$

Factor out the common term $\frac{1}{2}k A^2$:

$$
\begin{align}
E(t) &= \frac{1}{2}k A^2 \left[ \sin^2(\omega_0 t + \phi) + \cos^2(\omega_0 t + \phi) \right] \\
     &= \frac{1}{2}k A^2 (1) \\
     &= \frac{1}{2}k A^2
\end{align}
$$

Since $k$ and $A$ are constants, $E(t)$ is strictly independent of time $t$. Energy is conserved.

### 5. Interpretation in phase space

Consider the normalized coordinates in phase space. Rearrange the total energy equation:

$$
\frac{1}{2}m v^2 + \frac{1}{2}k x^2 = E
$$

Divide the entire equation by $E$:

$$
\frac{x^2}{\frac{2E}{k}} + \frac{v^2}{\frac{2E}{m}} = 1
$$

This is the standard equation of an ellipse in the $(x, v)$ plane. The semi-major and semi-minor axes are defined by the maximum displacement $x_{max} = \sqrt{2E/k}$ and maximum velocity $v_{max} = \sqrt{2E/m}$.

## Final Result

- $x(t) = A \cos(\omega_0 t + \phi)$
- $\omega_0 = \sqrt{\frac{k}{m}}$
- $E(t) = \frac{1}{2}k A^2$
- $E(t)$ is mathematically constant.
- The phase space trajectory forms a closed ellipse.

## Interpretation

The conservative nature of the harmonic oscillator guarantees that the system exchanges kinetic and potential energy perfectly without dissipation. The closed elliptical loop in phase space signifies a bounded, periodic, and deterministic dynamic system that will trace the identical orbit infinitely.