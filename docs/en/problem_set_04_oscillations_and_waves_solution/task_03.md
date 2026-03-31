# Task 03 – Harmonic wave

## Problem Statement

The wave equation is given:

$$
y(x,t) = A \sin(kx - \omega t)
$$

Determine:
1. The wavelength $\lambda$.
2. The phase velocity $v$.
3. The phase velocity $v$ for $k = 4\pi\ \mathrm{m^{-1}}$ and $\omega = 20\pi\ \mathrm{rad/s}$.
4. Whether the point $x = \lambda$ oscillates in phase with the point $x = 0$.

## Theory

A harmonic wave is periodic in both space and time. 
- The wavenumber $k$ dictates the spatial periodicity (wavelength $\lambda$).
- The angular frequency $\omega$ dictates the temporal periodicity (period $T$).

The phase velocity $v$ is the speed at which a surface of constant phase propagates through space.

Two points oscillate in phase if the difference between their phase angles is an integer multiple of $2\pi$.

## Step-by-Step Solution

### 1. Wavelength

The spatial period of the sine function is $2\pi$. Therefore, increasing $x$ by one wavelength $\lambda$ must increase the phase by $2\pi$:

$$
k(x + \lambda) - kx = 2\pi
$$

$$
k\lambda = 2\pi
$$

$$
\lambda = \frac{2\pi}{k}
$$

### 2. Phase velocity

To find the phase velocity, set the phase to a constant:

$$
kx - \omega t = \text{const}
$$

Differentiate with respect to time $t$:

$$
k \frac{dx}{dt} - \omega = 0
$$

Since $v = \frac{dx}{dt}$:

$$
kv = \omega
$$

$$
v = \frac{\omega}{k}
$$

### 3. Calculation for specific parameters

Given $k = 4\pi$ and $\omega = 20\pi$:

$$
\begin{align}
v &= \frac{20\pi}{4\pi} \\
  &= 5\ \mathrm{m/s}
\end{align}
$$

### 4. Phase comparison between $x = 0$ and $x = \lambda$

Evaluate the phase of the wave at $x = 0$:

$$
\varphi_1(t) = k(0) - \omega t = -\omega t
$$

Evaluate the phase of the wave at $x = \lambda$:

$$
\varphi_2(t) = k\lambda - \omega t
$$

Substitute $k = \frac{2\pi}{\lambda}$:

$$
\begin{align}
\varphi_2(t) &= \left( \frac{2\pi}{\lambda} \right) \lambda - \omega t \\
             &= 2\pi - \omega t
\end{align}
$$

Compute the phase difference $\Delta \varphi$:

$$
\begin{align}
\Delta \varphi &= \varphi_2(t) - \varphi_1(t) \\
               &= (2\pi - \omega t) - (-\omega t) \\
               &= 2\pi
\end{align}
$$

Since the phase difference is exactly $2\pi$, the trigonometric functions yield identical values at all times $t$. Yes, the points oscillate perfectly in phase.

## Final Result

- $\lambda = \frac{2\pi}{k}$
- $v = \frac{\omega}{k}$
- $v = 5\ \mathrm{m/s}$
- Yes, $x = \lambda$ oscillates in phase with $x = 0$.

## Interpretation

The wave function models a disturbance moving in the positive $x$-direction. The wavelength defines the minimum spatial distance between two identical states of the medium at a frozen instant in time. Consequently, any two points separated by exactly one wavelength will experience the identical disturbance history, merely shifted in time by one full period.