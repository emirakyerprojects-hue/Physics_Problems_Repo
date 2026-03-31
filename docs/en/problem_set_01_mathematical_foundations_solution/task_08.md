# Task 08 – First-order differential equation

## Problem Statement

Given the first-order differential equation:

$$
\frac{dy}{dt} = -k y
$$

Determine:
1. The analytical solution $y(t)$ for a given initial condition $y(0)$.
2. The mathematical framework required to visualize the solution for various values of the parameter $k$.

## Theory

A differential equation where the rate of change of a quantity is proportional to the quantity itself is solved using the method of separation of variables. This specific form describes natural exponential decay (if $k > 0$) or exponential growth (if $k < 0$).

## Step-by-Step Solution

### 1. Analytical Solution

Start by separating the variables $y$ and $t$ to opposite sides of the equation:

$$
\frac{dy}{y} = -k \, dt
$$

Integrate both sides:

$$
\int \frac{1}{y} \, dy = \int -k \, dt
$$

$$
\ln|y| = -kt + C
$$

Exponentiate both sides to solve for $y$:

$$
\begin{align}
|y| &= e^{-kt + C} \\
    &= e^C e^{-kt}
\end{align}
$$

Let $A = \pm e^C$, which acts as a new arbitrary constant. This allows the removal of the absolute value:

$$
y(t) = A e^{-kt}
$$

To find the constant $A$, apply the initial condition at $t=0$:

$$
\begin{align}
y(0) &= A e^{-k(0)} \\
     &= A(1) \\
     &= A
\end{align}
$$

Substituting $A$ back into the general solution yields the particular solution:

$$
y(t) = y(0) e^{-kt}
$$

### 2. Framework for Visualization

To plot this computationally, the continuous function must be evaluated at discrete time steps. For an array of time values $t_i$ ranging from $0$ to $t_{max}$, compute the corresponding $y_i$:

$$
y_i = y(0) e^{-k t_i}
$$

Varying $k$ alters the steepness of the curve. A larger positive $k$ will result in a more rapid decay towards zero, while $y(0)$ solely determines the $y$-intercept.

## Final Result

- $y(t) = y(0) e^{-kt}$

## Interpretation

The solution represents an exponential function. In physical systems, this mathematical model commonly describes radioactive decay, the discharging of a capacitor through a resistor, or the cooling of an object in a constant-temperature environment (Newton's law of cooling). The constant $k$ defines the characteristic timescale of the system, often denoted as $\tau = 1/k$.