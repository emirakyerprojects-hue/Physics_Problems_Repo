# Task 09 – Harmonic oscillator

## Problem Statement

Given the differential equation for a simple harmonic oscillator:

$$
\frac{d^2 x}{dt^2} + \omega^2 x = 0
$$

Determine:
1. The general solution $x(t)$.
2. The particular solution for the initial position $x(0) = x_0$ and initial velocity $x'(0) = v_0$.
3. The expressions for $x(t)$, $x'(t)$, and $x''(t)$ to be used in numerical visualization.

## Theory

The given equation is a linear, homogeneous, second-order ordinary differential equation with constant coefficients. It describes a system where the restoring force is directly proportional to the displacement from equilibrium (Hooke's Law).

The general solution is found by proposing an exponential ansatz $x(t) = e^{rt}$, which leads to a characteristic polynomial. Complex roots of this polynomial yield oscillatory solutions via Euler's formula.

## Step-by-Step Solution

### 1. General Solution

Substitute $x(t) = e^{rt}$ into the differential equation to obtain the characteristic equation:

$$
r^2 e^{rt} + \omega^2 e^{rt} = 0
$$

Since $e^{rt} \neq 0$:

$$
r^2 + \omega^2 = 0
$$

$$
r = \pm i\omega
$$

The roots are purely imaginary. The general complex solution is:

$$
x(t) = C_a e^{i\omega t} + C_b e^{-i\omega t}
$$

Using Euler's formula ($e^{i\theta} = \cos\theta + i\sin\theta$), this can be rewritten in terms of real-valued functions with new real constants $C_1$ and $C_2$:

$$
x(t) = C_1 \cos(\omega t) + C_2 \sin(\omega t)
$$

### 2. Particular Solution

To find $C_1$ and $C_2$, apply the initial conditions.

First, use the initial position $x(0) = x_0$:

$$
\begin{align}
x(0) &= C_1 \cos(0) + C_2 \sin(0) \\
     &= C_1(1) + C_2(0) \\
     &= C_1
\end{align}
$$

Thus, $C_1 = x_0$.

Next, find the first derivative $x'(t)$ to apply the initial velocity condition:

$$
x'(t) = -C_1 \omega \sin(\omega t) + C_2 \omega \cos(\omega t)
$$

Apply $x'(0) = v_0$:

$$
\begin{align}
x'(0) &= -x_0 \omega \sin(0) + C_2 \omega \cos(0) \\
      &= 0 + C_2 \omega \\
      &= C_2 \omega
\end{align}
$$

$$
C_2 = \frac{v_0}{\omega}
$$

Substitute the constants back into the general solution:

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)
$$

### 3. Kinematic Equations for Visualization

To plot the full state of the oscillator, the equations for position, velocity, and acceleration are required:

**Position:**

$$
x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)
$$

**Velocity ($x'(t)$):**

$$
v(t) = -x_0 \omega \sin(\omega t) + v_0 \cos(\omega t)
$$

**Acceleration ($x''(t)$):**

Differentiating the velocity, or rearranging the original differential equation ($x'' = -\omega^2 x$):

$$
a(t) = -\omega^2 \left( x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t) \right)
$$

## Final Result

- $x(t) = x_0 \cos(\omega t) + \frac{v_0}{\omega} \sin(\omega t)$
- $x'(t) = -x_0 \omega \sin(\omega t) + v_0 \cos(\omega t)$
- $x''(t) = -\omega^2 x(t)$

## Interpretation

The system exhibits perpetual, undamped sinusoidal motion. The initial displacement defines the amplitude of the cosine component, while the initial velocity defines the amplitude of the sine component. The acceleration is always opposite in sign to the displacement, enforcing the restoring nature of the physical force (e.g., a spring mass system).