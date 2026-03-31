# Task 05 – Elliptical motion (purely kinematic)

## Problem Statement

The path equation is given in parametric form:

$$
x(t) = a\cos(\omega t), \qquad y(t) = b\sin(\omega t)
$$

Determine:
1. The velocity $\vec v(t)$ and acceleration $\vec a(t)$.
2. Whether the magnitude of the velocity $|\vec v(t)|$ is constant.
3. The locations on the trajectory where the velocity is maximum.
4. The geometric features required to draw the trajectory and the graphs of $|\vec v(t)|$ and $|\vec a(t)|$.

## Theory

Elliptical motion generalizes circular motion by assigning different amplitudes ($a$ and $b$) to orthogonal harmonic oscillations of the same frequency $\omega$. 

The properties of the motion depend on the eccentricity of the ellipse. The magnitudes of the kinematic vectors will fluctuate continuously as the particle moves through different regions of curvature.

## Step-by-Step Solution

### 1. Velocity and Acceleration

Differentiate the position components with respect to time to obtain the velocity:

$$
\begin{align}
\vec v(t) &= \left( \frac{d}{dt}(a\cos(\omega t)), \frac{d}{dt}(b\sin(\omega t)) \right) \\
          &= \bigl(-a\omega\sin(\omega t), b\omega\cos(\omega t)\bigr)
\end{align}
$$

Differentiate the velocity components to obtain the acceleration:

$$
\begin{align}
\vec a(t) &= \left( \frac{d}{dt}(-a\omega\sin(\omega t)), \frac{d}{dt}(b\omega\cos(\omega t)) \right) \\
          &= \bigl(-a\omega^2\cos(\omega t), -b\omega^2\sin(\omega t)\bigr)
\end{align}
$$

Note that $\vec a(t) = -\omega^2 \vec r(t)$, indicating that the acceleration is always directed towards the center of the ellipse.

### 2. Magnitude of Velocity

Compute the Euclidean norm of the velocity vector:

$$
|\vec v(t)| = \sqrt{(-a\omega\sin(\omega t))^2 + (b\omega\cos(\omega t))^2}
$$

$$
|\vec v(t)| = \omega \sqrt{a^2\sin^2(\omega t) + b^2\cos^2(\omega t)}
$$

Because $a \neq b$ (in a general ellipse), the sum under the square root does not simplify to a constant scalar. The magnitude of the velocity depends explicitly on time $t$. Therefore, the speed is not constant.

### 3. Maximum Velocity

To find where the velocity is maximum, analyze the radicand $f(t) = a^2\sin^2(\omega t) + b^2\cos^2(\omega t)$.
Assume, without loss of generality, that $a > b$ (meaning the ellipse is wider along the $x$-axis).

Substitute $\cos^2(\omega t) = 1 - \sin^2(\omega t)$:

$$
\begin{align}
f(t) &= a^2\sin^2(\omega t) + b^2(1 - \sin^2(\omega t)) \\
     &= b^2 + (a^2 - b^2)\sin^2(\omega t)
\end{align}
$$

Since $(a^2 - b^2) > 0$, the function $f(t)$ reaches its maximum when $\sin^2(\omega t) = 1$. This occurs when:

$$
\omega t = \frac{\pi}{2}, \frac{3\pi}{2}, \dots
$$

At these times, the physical coordinates are:

$$
x = a\cos\left(\frac{\pi}{2}\right) = 0
$$

$$
y = b\sin\left(\frac{\pi}{2}\right) = \pm b
$$

Thus, the velocity magnitude is maximized at the ends of the minor axis $(0, \pm b)$. Conversely, the speed is minimized at the ends of the major axis $(\pm a, 0)$.

### 4. Trajectory and Graphs

- **Trajectory:** An ellipse centered at the origin intersecting the axes at $(\pm a, 0)$ and $(0, \pm b)$.
- **Graph of $|\vec v(t)|$:** An oscillating non-sinusoidal periodic function bounding between $\omega b$ and $\omega a$.
- **Graph of $|\vec a(t)|$:** The acceleration magnitude is $|\vec a(t)| = \omega^2 \sqrt{a^2\cos^2(\omega t) + b^2\sin^2(\omega t)}$. This function oscillates perfectly out of phase with the velocity; it is maximum at the major axis vertices and minimum at the minor axis vertices.

## Final Result

- $\vec v(t) = \bigl(-a\omega\sin(\omega t), b\omega\cos(\omega t)\bigr)$
- $\vec a(t) = \bigl(-a\omega^2\cos(\omega t), -b\omega^2\sin(\omega t)\bigr)$
- $|\vec v(t)|$ is not constant.
- Maximum velocity occurs at the endpoints of the minor axis ($y$-intercepts if $a>b$).

## Interpretation

In purely kinematic elliptical motion where the angle varies linearly with time ($\theta = \omega t$), the particle sweeps through different regions of the path at varying speeds. The particle must travel fastest when crossing the minor axis because the radius vector is shortest, yet it must sweep through an equivalent angular displacement in the same time interval.