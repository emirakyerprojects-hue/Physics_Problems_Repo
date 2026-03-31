# Task 01 – Harmonic motion: motion parameters

## Problem Statement

A function describing harmonic motion is given:

$$
x(t) = A \cos(\omega t + \varphi)
$$

Determine:
1. The period $T$ and the frequency $f$.
2. The maximum velocity $v_{\max}$ and the maximum acceleration $a_{\max}$.
3. For $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$, calculate $\omega$, $v_{\max}$, and $a_{\max}$.

## Theory

Simple harmonic motion is a sinusoidal, periodic motion. The argument of the trigonometric function, $(\omega t + \varphi)$, is the phase. The angular frequency $\omega$ determines how rapidly the phase changes with time. 

Kinematic variables are derived by taking successive time derivatives of the position function. The maximum values of these variables correspond to the amplitudes of the resulting sinusoidal functions.

## Step-by-Step Solution

### 1. Period and frequency

The angular frequency $\omega$ is related to the period $T$ (the time for one complete cycle) by:

$$
\omega = \frac{2\pi}{T}
$$

Rearranging for $T$:

$$
T = \frac{2\pi}{\omega}
$$

The frequency $f$ is the reciprocal of the period:

$$
f = \frac{1}{T} = \frac{\omega}{2\pi}
$$

### 2. Maximum velocity and acceleration

Differentiate the position $x(t)$ with respect to time to find the velocity $v(t)$:

$$
\begin{align}
v(t) &= \frac{dx}{dt} \\
     &= \frac{d}{dt} [A \cos(\omega t + \varphi)] \\
     &= -A\omega \sin(\omega t + \varphi)
\end{align}
$$

The sine function oscillates between $-1$ and $1$. The maximum magnitude of velocity is the coefficient:

$$
v_{\max} = A\omega
$$

Differentiate the velocity $v(t)$ to find the acceleration $a(t)$:

$$
\begin{align}
a(t) &= \frac{dv}{dt} \\
     &= \frac{d}{dt} [-A\omega \sin(\omega t + \varphi)] \\
     &= -A\omega^2 \cos(\omega t + \varphi)
\end{align}
$$

The cosine function oscillates between $-1$ and $1$. The maximum magnitude of acceleration is:

$$
a_{\max} = A\omega^2
$$

### 3. Calculations for specific parameters

Given $A = 0.2\ \mathrm{m}$ and $f = 2\ \mathrm{Hz}$.

Calculate the angular frequency $\omega$:

$$
\begin{align}
\omega &= 2\pi f \\
       &= 2\pi (2) \\
       &= 4\pi\ \mathrm{rad/s} \approx 12.57\ \mathrm{rad/s}
\end{align}
$$

Calculate the maximum velocity $v_{\max}$:

$$
\begin{align}
v_{\max} &= A\omega \\
         &= (0.2)(4\pi) \\
         &= 0.8\pi\ \mathrm{m/s} \approx 2.51\ \mathrm{m/s}
\end{align}
$$

Calculate the maximum acceleration $a_{\max}$:

$$
\begin{align}
a_{\max} &= A\omega^2 \\
         &= (0.2)(4\pi)^2 \\
         &= (0.2)(16\pi^2) \\
         &= 3.2\pi^2\ \mathrm{m/s^2} \approx 31.58\ \mathrm{m/s^2}
\end{align}
$$

## Final Result

- $T = \frac{2\pi}{\omega}$
- $f = \frac{\omega}{2\pi}$
- $v_{\max} = A\omega$
- $a_{\max} = A\omega^2$
- For $A=0.2\ \mathrm{m}, f=2\ \mathrm{Hz}$: $\omega = 4\pi\ \mathrm{rad/s}$, $v_{\max} = 0.8\pi\ \mathrm{m/s}$, $a_{\max} = 3.2\pi^2\ \mathrm{m/s^2}$.

## Interpretation

The velocity reaches its maximum magnitude when the displacement is zero (at the equilibrium position), as the sine function peaks when the cosine is zero. Conversely, the acceleration reaches its maximum magnitude when the displacement is maximal (at the turning points), reflecting the strongest restoring force.