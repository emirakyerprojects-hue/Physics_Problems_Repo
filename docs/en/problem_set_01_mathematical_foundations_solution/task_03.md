# Task 03 – Integration of motion

## Problem Statement

### Part A
Given velocity and initial position:

$$
\vec v(t) = \bigl(2t, 3, -e^{-t}\bigr), \qquad \vec r(0) = (0, 1, 2)
$$

Determine $\vec r(t)$ and $\vec a(t)$.

### Part B
Given acceleration, initial velocity, and initial position:

$$
\vec a(t) = \bigl(4, -\sin t, 0\bigr), \qquad \vec v(0) = (1, 0, 2), \qquad \vec r(0) = (0, 0, 0)
$$

Determine $\vec v(t)$ and $\vec r(t)$.

## Theory

Kinematic quantities are related through fundamental calculus operations. Position is the time integral of velocity, and velocity is the time integral of acceleration. Initial conditions serve as constants of integration.

Position from velocity:

$$
\vec r(t) = \vec r(0) + \int_0^t \vec v(\tau)\, d\tau
$$

Velocity from acceleration:

$$
\vec v(t) = \vec v(0) + \int_0^t \vec a(\tau)\, d\tau
$$

Acceleration from velocity is obtained via differentiation:

$$
\vec a(t) = \frac{d\vec v}{dt}
$$

## Step-by-Step Solution

### Part A

**1. Position vector $\vec r(t)$**

Integrate the velocity vector with respect to time:

$$
\begin{align}
\int_0^t \vec v(\tau) \, d\tau &= \int_0^t \bigl(2\tau, 3, -e^{-\tau}\bigr) \, d\tau \\
                               &= \left[ \tau^2, 3\tau, e^{-\tau} \right]_0^t \\
                               &= (t^2 - 0, 3t - 0, e^{-t} - e^0) \\
                               &= (t^2, 3t, e^{-t} - 1)
\end{align}
$$

Add the initial position:

$$
\begin{align}
\vec r(t) &= (0, 1, 2) + (t^2, 3t, e^{-t} - 1) \\
          &= (t^2, 1 + 3t, 1 + e^{-t})
\end{align}
$$

**2. Acceleration vector $\vec a(t)$**

Differentiate the velocity vector:

$$
\begin{align}
\vec a(t) &= \frac{d}{dt} \bigl(2t, 3, -e^{-t}\bigr) \\
          &= \bigl(2, 0, e^{-t}\bigr)
\end{align}
$$

### Part B

**1. Velocity vector $\vec v(t)$**

Integrate the acceleration vector:

$$
\begin{align}
\int_0^t \vec a(\tau) \, d\tau &= \int_0^t \bigl(4, -\sin\tau, 0\bigr) \, d\tau \\
                               &= \left[ 4\tau, \cos\tau, 0 \right]_0^t \\
                               &= (4t - 0, \cos t - \cos 0, 0) \\
                               &= (4t, \cos t - 1, 0)
\end{align}
$$

Add the initial velocity:

$$
\begin{align}
\vec v(t) &= (1, 0, 2) + (4t, \cos t - 1, 0) \\
          &= (1 + 4t, \cos t - 1, 2)
\end{align}
$$

**2. Position vector $\vec r(t)$**

Integrate the newly found velocity vector:

$$
\begin{align}
\int_0^t \vec v(\tau) \, d\tau &= \int_0^t (1 + 4\tau, \cos\tau - 1, 2) \, d\tau \\
                               &= \left[ \tau + 2\tau^2, \sin\tau - \tau, 2\tau \right]_0^t \\
                               &= (t + 2t^2, \sin t - t, 2t)
\end{align}
$$

Add the initial position:

$$
\begin{align}
\vec r(t) &= (0, 0, 0) + (t + 2t^2, \sin t - t, 2t) \\
          &= (t + 2t^2, \sin t - t, 2t)
\end{align}
$$

## Final Result

**Part A**
- $\vec r(t) = (t^2, 1 + 3t, 1 + e^{-t})$
- $\vec a(t) = (2, 0, e^{-t})$

**Part B**
- $\vec v(t) = (1 + 4t, \cos t - 1, 2)$
- $\vec r(t) = (t + 2t^2, \sin t - t, 2t)$

## Interpretation

Integration allows the full determination of the state of motion provided the initial conditions (constants of integration) are known. In Part A, an exponentially decaying term in velocity translates to a corresponding decay in acceleration and a specific bound asymptote in the $z$-axis position over time.