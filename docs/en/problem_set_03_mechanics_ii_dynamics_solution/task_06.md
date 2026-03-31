# Task 06 – Motion with linear drag

## Problem Statement

The drag force is given by the formula:

$$
F = -kv
$$

Initial conditions: $v(0) = v_0$, $x(0) = 0$.

Determine:
1. The equation of motion and its solution for $v(t)$ and $x(t)$.
2. The limit $\lim_{t\to\infty} v(t)$.
3. The comparison with motion without drag.

## Theory

A drag force proportional to the first power of velocity typically models an object moving through a viscous fluid at low Reynolds numbers (Stokes' drag). 

Newton's second law generates a first-order separable ordinary differential equation for the velocity. Integrating the velocity function yields the position function.

## Step-by-Step Solution

### 1. Equation of motion and solution

Write Newton's second law:

$$
m \frac{dv}{dt} = -kv
$$

Separate the variables $v$ and $t$:

$$
\frac{dv}{v} = -\frac{k}{m} dt
$$

Integrate both sides:

$$
\int \frac{1}{v} \, dv = \int -\frac{k}{m} \, dt
$$

$$
\ln(v) = -\frac{k}{m} t + C
$$

Exponentiate to solve for $v$:

$$
v(t) = e^C e^{-\frac{k}{m}t}
$$

Apply the initial condition $v(0) = v_0$:

$$
v_0 = e^C e^0 \implies e^C = v_0
$$

The velocity as a function of time is:

$$
v(t) = v_0 e^{-\frac{k}{m}t}
$$

To find the position $x(t)$, integrate the velocity:

$$
\begin{align}
x(t) &= \int v(t) \, dt \\
     &= \int v_0 e^{-\frac{k}{m}t} \, dt \\
     &= -\frac{m v_0}{k} e^{-\frac{k}{m}t} + C_2
\end{align}
$$

Apply the initial condition $x(0) = 0$:

$$
0 = -\frac{m v_0}{k} (1) + C_2 \implies C_2 = \frac{m v_0}{k}
$$

The position as a function of time is:

$$
\begin{align}
x(t) &= \frac{m v_0}{k} - \frac{m v_0}{k} e^{-\frac{k}{m}t} \\
     &= \frac{m v_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)
\end{align}
$$

### 2. Limit at infinity

Investigate the velocity limit as $t \to \infty$:

$$
\begin{align}
\lim_{t \to \infty} v(t) &= \lim_{t \to \infty} v_0 e^{-\frac{k}{m}t} \\
                         &= 0
\end{align}
$$

Investigate the position limit as $t \to \infty$:

$$
\begin{align}
\lim_{t \to \infty} x(t) &= \lim_{t \to \infty} \frac{m v_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right) \\
                         &= \frac{m v_0}{k} (1 - 0) \\
                         &= \frac{m v_0}{k}
\end{align}
$$

### 3. Comparison with motion without drag

**Without drag ($k = 0$):**
- Acceleration is zero ($a = 0$).
- Velocity is constant ($v(t) = v_0$). 
- The limit of velocity at infinity is $v_0$.
- Position grows linearly without bound ($x(t) = v_0 t$). 

**With drag ($k > 0$):**
- Acceleration decreases exponentially towards zero.
- Velocity decays exponentially towards zero.
- The position is strictly bounded. The body comes to a halt asymptotically, covering a maximum finite stopping distance of $x_{max} = \frac{m v_0}{k}$.

## Final Result

- Equation of motion: $m \frac{dv}{dt} = -kv$
- $v(t) = v_0 e^{-\frac{k}{m}t}$
- $x(t) = \frac{m v_0}{k} \left( 1 - e^{-\frac{k}{m}t} \right)$
- $\lim_{t\to\infty} v(t) = 0$
- The drag force bounds the total distance traveled, unlike the undamped counterpart where the object coasts forever.

## Interpretation

The linear drag force dissipates kinetic energy continuously as heat into the surrounding fluid. Because the drag force decreases as the object slows down, the object never strictly reaches zero velocity in finite time mathematically, but the total displacement converges to a finite value due to the rapid exponential decay of the speed.