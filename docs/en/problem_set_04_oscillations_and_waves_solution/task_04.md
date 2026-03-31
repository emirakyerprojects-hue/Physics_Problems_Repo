# Task 04 – Wave equation

## Problem Statement

The function is given:

$$
y(x,t) = A \cos(kx - \omega t)
$$

Determine:
1. The verification that it satisfies the one-dimensional wave equation:
$$
\frac{\partial^2 y}{\partial t^2} = v^2 \frac{\partial^2 y}{\partial x^2}
$$
2. The algebraic relationship between the phase velocity $v$, the wavenumber $k$, and the angular frequency $\omega$.

## Theory

The standard one-dimensional linear wave equation is a second-order partial differential equation that describes the propagation of waves at a constant speed $v$. 

Any function of the form $f(x \pm vt)$ is a valid solution to this equation. For a harmonic wave represented by trigonometric functions, substituting the partial derivatives back into the wave equation reveals the fundamental dispersion relation of the medium.

## Step-by-Step Solution

### 1. Verifying the wave equation

First, calculate the first and second partial derivatives of the wave function with respect to time $t$. Treat $x$ as a constant:

$$
\begin{align}
\frac{\partial y}{\partial t} &= \frac{\partial}{\partial t} [A \cos(kx - \omega t)] \\
                              &= -A \sin(kx - \omega t) \cdot (-\omega) \\
                              &= A \omega \sin(kx - \omega t)
\end{align}
$$

$$
\begin{align}
\frac{\partial^2 y}{\partial t^2} &= \frac{\partial}{\partial t} [A \omega \sin(kx - \omega t)] \\
                                  &= A \omega \cos(kx - \omega t) \cdot (-\omega) \\
                                  &= -A \omega^2 \cos(kx - \omega t)
\end{align}
$$

Next, calculate the first and second partial derivatives of the wave function with respect to position $x$. Treat $t$ as a constant:

$$
\begin{align}
\frac{\partial y}{\partial x} &= \frac{\partial}{\partial x} [A \cos(kx - \omega t)] \\
                              &= -A \sin(kx - \omega t) \cdot (k) \\
                              &= -A k \sin(kx - \omega t)
\end{align}
$$

$$
\begin{align}
\frac{\partial^2 y}{\partial x^2} &= \frac{\partial}{\partial x} [-A k \sin(kx - \omega t)] \\
                                  &= -A k \cos(kx - \omega t) \cdot (k) \\
                                  &= -A k^2 \cos(kx - \omega t)
\end{align}
$$

Notice that the original function $y(x,t) = A \cos(kx - \omega t)$ appears in both second derivatives:

$$
\frac{\partial^2 y}{\partial t^2} = -\omega^2 y(x,t)
$$

$$
\frac{\partial^2 y}{\partial x^2} = -k^2 y(x,t)
$$

Substitute these expressions into the given wave equation:

$$
-\omega^2 y(x,t) = v^2 (-k^2 y(x,t))
$$

Divide both sides by $-y(x,t)$ (assuming $y \neq 0$):

$$
\omega^2 = v^2 k^2
$$

Since $v$, $\omega$, and $k$ are strictly positive physical quantities, taking the square root yields:

$$
\omega = v k
$$

This equality holds true, thus verifying that the function satisfies the wave equation.

### 2. Relationship between $v$, $k$, and $\omega$

Rearranging the derived equality yields the definition of the phase velocity:

$$
v = \frac{\omega}{k}
$$

## Final Result

- $\frac{\partial^2 y}{\partial t^2} = -\omega^2 A \cos(kx - \omega t)$
- $\frac{\partial^2 y}{\partial x^2} = -k^2 A \cos(kx - \omega t)$
- $v = \frac{\omega}{k}$

## Interpretation

The wave equation strictly requires the ratio of the temporal curvature (acceleration of the medium's particles) to the spatial curvature (the bending of the wave string) to be constant. This constant is exactly the square of the wave propagation speed, establishing the fundamental link between space, time, and the medium's properties.