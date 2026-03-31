# Task 04 – Circular motion

## Problem Statement

A body moves in a circle of radius $R$ with angular velocity $\omega$. 

Determine:
1. The position vector $\vec r(t)$, velocity vector $\vec v(t)$, and acceleration vector $\vec a(t)$.
2. The magnitudes $|\vec r(t)|$, $|\vec v(t)|$, and $|\vec a(t)|$.
3. Prove mathematically that the acceleration is centripetal.
4. The geometric relationship required to visualize the vectors $\vec r$, $\vec v$, and $\vec a$.

## Theory

Uniform circular motion in a two-dimensional plane is described by parametric equations utilizing sine and cosine functions. The angle $\theta$ traversed in time $t$ is given by $\theta(t) = \omega t$, where $\omega$ is the constant angular velocity. 

Centripetal acceleration is defined as an acceleration vector that points strictly towards the center of curvature. Mathematically, this implies that the acceleration vector is anti-parallel to the position vector (relative to the center of the circle).

## Step-by-Step Solution

### 1. Kinematic vectors

Define the origin at the center of the circle. The position vector is:

$$
\vec r(t) = \bigl( R\cos(\omega t), R\sin(\omega t) \bigr)
$$

The velocity is the first time derivative of the position:

$$
\begin{align}
\vec v(t) &= \frac{d}{dt} \bigl( R\cos(\omega t), R\sin(\omega t) \bigr) \\
          &= \bigl( -R\omega\sin(\omega t), R\omega\cos(\omega t) \bigr)
\end{align}
$$

The acceleration is the first time derivative of the velocity:

$$
\begin{align}
\vec a(t) &= \frac{d}{dt} \bigl( -R\omega\sin(\omega t), R\omega\cos(\omega t) \bigr) \\
          &= \bigl( -R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t) \bigr)
\end{align}
$$

### 2. Magnitudes

Calculate the Euclidean norm for each vector.

**Position magnitude:**

$$
\begin{align}
|\vec r(t)| &= \sqrt{(R\cos(\omega t))^2 + (R\sin(\omega t))^2} \\
            &= \sqrt{R^2 (\cos^2(\omega t) + \sin^2(\omega t))} \\
            &= R
\end{align}
$$

**Velocity magnitude:**

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-R\omega\sin(\omega t))^2 + (R\omega\cos(\omega t))^2} \\
            &= \sqrt{R^2\omega^2 (\sin^2(\omega t) + \cos^2(\omega t))} \\
            &= R\omega
\end{align}
$$

**Acceleration magnitude:**

$$
\begin{align}
|\vec a(t)| &= \sqrt{(-R\omega^2\cos(\omega t))^2 + (-R\omega^2\sin(\omega t))^2} \\
            &= \sqrt{R^2\omega^4 (\cos^2(\omega t) + \sin^2(\omega t))} \\
            &= R\omega^2
\end{align}
$$

### 3. Proof of centripetal acceleration

Examine the expression derived for the acceleration vector:

$$
\vec a(t) = \bigl( -R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t) \bigr)
$$

Factor out the scalar term $-\omega^2$:

$$
\vec a(t) = -\omega^2 \bigl( R\cos(\omega t), R\sin(\omega t) \bigr)
$$

Substitute the original position vector $\vec r(t)$:

$$
\vec a(t) = -\omega^2 \vec r(t)
$$

Since $\omega^2$ is strictly positive, the vector $\vec a(t)$ points in the exact opposite direction to the position vector $\vec r(t)$. Because $\vec r(t)$ points outward from the origin (the center of the circle), $\vec a(t)$ must point strictly inward toward the origin. This proves the acceleration is centripetal.

### 4. Visualization

To visualize the system:
- $\vec r(t)$ is drawn from the origin to the particle's location.
- $\vec v(t)$ is drawn originating at the particle, tangent to the circular path (perpendicular to $\vec r(t)$ since $\vec r \cdot \vec v = 0$).
- $\vec a(t)$ is drawn originating at the particle, pointing backward along the line of $\vec r(t)$ toward the origin.

## Final Result

- $\vec r(t) = \bigl( R\cos(\omega t), R\sin(\omega t) \bigr)$
- $\vec v(t) = \bigl( -R\omega\sin(\omega t), R\omega\cos(\omega t) \bigr)$
- $\vec a(t) = \bigl( -R\omega^2\cos(\omega t), -R\omega^2\sin(\omega t) \bigr)$
- $|\vec r| = R$
- $|\vec v| = R\omega$
- $|\vec a| = R\omega^2$
- $\vec a(t) = -\omega^2 \vec r(t)$

## Interpretation

In uniform circular motion, the position, velocity, and acceleration vectors maintain constant magnitudes but continuously change direction. The velocity vector is purely tangential, while the acceleration vector is purely normal (centripetal). This normal acceleration performs no work and strictly acts to rotate the velocity vector without changing the particle's speed.