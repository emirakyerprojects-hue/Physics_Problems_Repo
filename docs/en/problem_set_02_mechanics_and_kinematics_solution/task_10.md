# Task 10 – Analysis of motion from numerical data

## Problem Statement

Given measurement data $x(t) = t + \frac{1}{20}t^2$ on the interval $t \in [0, 10]$ with a time step of $\Delta t = 0.1$:

Determine:
1. The approximation of velocity using finite differences.
2. The approximation of acceleration using finite differences.
3. The analytical solution for comparison.
4. The effect of the time step on accuracy.

## Theory

Numerical differentiation approximates the derivative of a function using discrete data points. 

The forward difference method for the first derivative (velocity) is:

$$
v_{approx}(t) = \frac{x(t + \Delta t) - x(t)}{\Delta t}
$$

The central difference method for the first derivative is:

$$
v_{central}(t) = \frac{x(t + \Delta t) - x(t - \Delta t)}{2\Delta t}
$$

The central difference method for the second derivative (acceleration) is:

$$
a_{approx}(t) = \frac{x(t + \Delta t) - 2x(t) + x(t - \Delta t)}{\Delta t^2}
$$

## Step-by-Step Solution

### 1. Analytical Solution (for baseline comparison)

Differentiate the given continuous function $x(t) = t + 0.05t^2$:

$$
v_{exact}(t) = \frac{d}{dt} \left( t + 0.05t^2 \right) = 1 + 0.1t
$$

$$
a_{exact}(t) = \frac{d}{dt} \left( 1 + 0.1t \right) = 0.1
$$

### 2. Velocity via Finite Difference

Apply the forward difference formula to $x(t)$:

$$
\begin{align}
v_{approx}(t) &= \frac{(t + \Delta t) + 0.05(t + \Delta t)^2 - (t + 0.05t^2)}{\Delta t} \\
              &= \frac{t + \Delta t + 0.05(t^2 + 2t\Delta t + \Delta t^2) - t - 0.05t^2}{\Delta t} \\
              &= \frac{\Delta t + 0.1t\Delta t + 0.05\Delta t^2}{\Delta t} \\
              &= 1 + 0.1t + 0.05\Delta t
\end{align}
$$

If $\Delta t = 0.1$:

$$
v_{approx}(t) = 1 + 0.1t + 0.005
$$

### 3. Acceleration via Finite Difference

Apply the central difference formula to $x(t)$ for the second derivative:

Let $x_1 = x(t + \Delta t)$ and $x_{-1} = x(t - \Delta t)$.

$$
x_1 = t + \Delta t + 0.05(t^2 + 2t\Delta t + \Delta t^2)
$$

$$
x_{-1} = t - \Delta t + 0.05(t^2 - 2t\Delta t + \Delta t^2)
$$

Substitute into the central difference formula:

$$
\begin{align}
a_{approx}(t) &= \frac{x_1 - 2x(t) + x_{-1}}{\Delta t^2} \\
              &= \frac{2t + 0.1t^2 + 0.1\Delta t^2 - 2(t + 0.05t^2)}{\Delta t^2} \\
              &= \frac{0.1\Delta t^2}{\Delta t^2} \\
              &= 0.1
\end{align}
$$

### 4. Effect of time step on accuracy

The error in the forward difference approximation for velocity is:

$$
\begin{align}
E_v &= v_{approx}(t) - v_{exact}(t) \\
    &= (1 + 0.1t + 0.05\Delta t) - (1 + 0.1t) \\
    &= 0.05\Delta t
\end{align}
$$

This demonstrates a first-order error $O(\Delta t)$. As the time step $\Delta t$ decreases, the numerical approximation linearly converges to the exact analytical value.

For the acceleration, the central difference method yielded exactly $0.1$, which perfectly matches $a_{exact}$. The central difference approximation for a purely quadratic polynomial has zero truncation error regardless of the time step size, because the third and higher-order derivatives of a parabola are zero.

## Final Result

- Analytical: $v(t) = 1 + 0.1t$, $a(t) = 0.1$
- Forward Difference $v$: $v(t) \approx 1 + 0.1t + 0.05\Delta t$
- Central Difference $a$: $a(t) \approx 0.1$

## Interpretation

Numerical differentiation introduces truncation errors that scale with the step size $\Delta t$. Forward and backward differences are strictly accurate only in the limit $\Delta t \to 0$. However, higher-order stencils like the central difference method can achieve exact solutions for low-order polynomial data without requiring infinitely small step sizes.