# Task 06 – Curve length and numerical integration

## Problem Statement

A parametric trajectory in 2D is given by:

$$
x(t) = t, \qquad y(t) = t^2, \qquad t \in [0,1]
$$

Determine:
1. The velocity vector $\vec v(t)$.
2. The magnitude of the velocity $|\vec v(t)|$.
3. The arc length integral $s$.
4. The analytical solution of the integral.
5. The mathematical formulation for numerical evaluation (e.g., trapezoidal rule) typically implemented in software.

## Theory

The arc length of a parametric curve from $t_a$ to $t_b$ is the integral of the speed (velocity magnitude) over that time interval:

$$
s = \int_{t_a}^{t_b} |\vec v(t)| \, dt
$$

Integrals involving $\sqrt{1+u^2}$ commonly arise in arc length calculations of parabolas and require hyperbolic trigonometric substitutions, such as $u = \sinh(\theta)$.

When analytical solutions are intractable or computationally expensive, numerical integration methods like the **Trapezoidal Rule** are employed. The interval $[a, b]$ is divided into $N$ subintervals of width $\Delta t$, and the area under the curve is approximated as a sum of trapezoids.

## Step-by-Step Solution

### 1. Velocity vector

$$
\begin{align}
\vec v(t) &= \left( \frac{dx}{dt}, \frac{dy}{dt} \right) \\
          &= (1, 2t)
\end{align}
$$

### 2. Magnitude of velocity

$$
|\vec v(t)| = \sqrt{1^2 + (2t)^2} = \sqrt{1 + 4t^2}
$$

### 3. Arc length integral

$$
s = \int_0^1 \sqrt{1 + 4t^2} \, dt
$$

### 4. Analytical calculation

Use the substitution $2t = \sinh u$. Then, the differential is $2 \, dt = \cosh u \, du$, or $dt = \frac{1}{2} \cosh u \, du$.

$$
\begin{align}
\int \sqrt{1 + 4t^2} \, dt &= \int \sqrt{1 + \sinh^2 u} \left(\frac{1}{2} \cosh u\right) du \\
                           &= \frac{1}{2} \int \cosh^2 u \, du
\end{align}
$$

Use the double-angle identity $\cosh^2 u = \frac{1 + \cosh(2u)}{2}$:

$$
\begin{align}
\frac{1}{2} \int \frac{1 + \cosh(2u)}{2} \, du &= \frac{1}{4} \left( u + \frac{1}{2}\sinh(2u) \right) \\
                                               &= \frac{1}{4} (u + \sinh u \cosh u)
\end{align}
$$

Substitute back $u = \text{arsinh}(2t) = \ln(2t + \sqrt{1 + 4t^2})$, $\sinh u = 2t$, and $\cosh u = \sqrt{1 + 4t^2}$:

$$
\int \sqrt{1 + 4t^2} \, dt = \frac{1}{4} \ln(2t + \sqrt{1 + 4t^2}) + \frac{1}{2} t \sqrt{1 + 4t^2}
$$

Evaluate from $t=0$ to $t=1$:

$$
\begin{align}
s &= \left[ \frac{1}{4} \ln(2(1) + \sqrt{1 + 4(1)^2}) + \frac{1}{2} (1) \sqrt{1 + 4(1)^2} \right] - [0 + 0] \\
  &= \frac{1}{4} \ln(2 + \sqrt{5}) + \frac{\sqrt{5}}{2}
\end{align}
$$

### 5. Numerical Integration Formulation (Trapezoidal Rule)

To evaluate $s$ programmatically, the continuous integral is replaced with a discrete sum. 

Let $f(t) = \sqrt{1 + 4t^2}$. Choose the number of divisions $N$. The step size is:

$$
\Delta t = \frac{1 - 0}{N} = \frac{1}{N}
$$

The trapezoidal rule approximation is:

$$
s \approx \frac{\Delta t}{2} \left[ f(t_0) + 2f(t_1) + 2f(t_2) + \dots + 2f(t_{N-1}) + f(t_N) \right]
$$

where $t_i = i \Delta t$.

*Note for programmatic implementation (JS structure):*
```javascript
let N = 100;
let dt = 1.0 / N;
let sum = 0.5 * (Math.sqrt(1) + Math.sqrt(1 + 4)); // Ends
for(let i = 1; i < N; i++) {
    let t = i * dt;
    sum += Math.sqrt(1 + 4 * t * t); // Middle terms
}
let s_approx = sum * dt;