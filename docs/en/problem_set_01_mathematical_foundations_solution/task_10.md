# Task 10 – Angular momentum in circular motion

## Problem Statement

Consider circular motion in the $xy$ plane given by:

$$
\vec r(t) = \bigl(R\cos(\omega t), \, R\sin(\omega t), \, 0\bigr)
$$

Determine:
1. The velocity vector $\vec v(t) = \dot{\vec r}(t)$.
2. The angular momentum with respect to the origin, $\vec L(t) = m\,\vec r(t) \times \vec v(t)$.
3. Whether $|\vec L|$ is constant and if $\vec L$ is perpendicular to the plane of motion.
4. The direction of $\vec L$ via the right-hand rule.
5. The torque $\vec \tau = \vec r \times \vec F$ given a centripetal force, verifying $\vec \tau = \frac{d\vec L}{dt}$.

## Theory

Angular momentum is the rotational equivalent of linear momentum, defined as the cross product of the position vector and the linear momentum vector ($\vec p = m\vec v$). 

Torque is the rotational equivalent of force. According to Newton's Second Law applied to rotation, the net external torque on a system equals the time rate of change of its angular momentum:

$$
\vec \tau = \frac{d\vec L}{dt}
$$

For uniform circular motion, the only acting force is the centripetal force, which points purely radially inward, parallel but opposite to the position vector.

## Step-by-Step Solution

### 1. Velocity

Take the time derivative of the position vector. The chain rule pulls out a factor of $\omega$:

$$
\begin{align}
\vec v(t) &= \frac{d}{dt} \bigl(R\cos(\omega t), R\sin(\omega t), 0\bigr) \\
          &= \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)
\end{align}
$$

### 2. Angular momentum

Compute the cross product $\vec r \times \vec v$:

$$
\begin{align}
\vec r \times \vec v &= 
\begin{pmatrix}
\hat i & \hat j & \hat k \\
R\cos(\omega t) & R\sin(\omega t) & 0 \\
-R\omega\sin(\omega t) & R\omega\cos(\omega t) & 0
\end{pmatrix} \\
&= \hat k \bigl( (R\cos(\omega t))(R\omega\cos(\omega t)) - (R\sin(\omega t))(-R\omega\sin(\omega t)) \bigr) \\
&= \hat k \bigl( R^2\omega\cos^2(\omega t) + R^2\omega\sin^2(\omega t) \bigr) \\
&= \hat k \bigl( R^2\omega (\cos^2(\omega t) + \sin^2(\omega t)) \bigr) \\
&= \bigl( 0, 0, R^2\omega \bigr)
\end{align}
$$

Multiply by mass $m$ to get $\vec L$:

$$
\vec L(t) = \bigl(0, 0, mR^2\omega\bigr)
$$

### 3. Magnitude and Perpendicularity

The magnitude is:

$$
|\vec L| = \sqrt{0^2 + 0^2 + (mR^2\omega)^2} = mR^2\omega
$$

Since $m$, $R$, and $\omega$ are all constants in uniform circular motion, $|\vec L|$ is strictly constant. 

Because the $x$ and $y$ components of $\vec L$ are zero, the vector lies entirely along the $z$-axis. The motion occurs purely in the $xy$ plane ($z=0$), so $\vec L$ is perfectly perpendicular to the plane of motion.

### 4. Right-Hand Rule Interpretation

If you curl the fingers of your right hand in the direction of the particle's orbit (from the positive $x$-axis towards the positive $y$-axis, assuming $\omega > 0$), your thumb points straight up along the positive $z$-axis. This perfectly matches the derived vector $\bigl(0, 0, mR^2\omega\bigr)$.

### 5. Torque and Rotational Dynamics

A central (centripetal) force points opposite to the position vector:

$$
\vec F = -m\omega^2 \vec r
$$

Calculate the torque $\vec \tau$:

$$
\begin{align}
\vec \tau &= \vec r \times \vec F \\
          &= \vec r \times (-m\omega^2 \vec r) \\
          &= -m\omega^2 (\vec r \times \vec r)
\end{align}
$$

Since the cross product of any vector with itself is the zero vector:

$$
\vec \tau = \vec 0
$$

Calculate the time derivative of angular momentum:

$$
\begin{align}
\frac{d\vec L}{dt} &= \frac{d}{dt} \bigl(0, 0, mR^2\omega\bigr) \\
                   &= \bigl(0, 0, 0\bigr) \\
                   &= \vec 0
\end{align}
$$

Thus, the relationship is verified:

$$
\vec \tau = \frac{d\vec L}{dt} = \vec 0
$$

## Final Result

- $\vec v(t) = \bigl(-R\omega\sin(\omega t), R\omega\cos(\omega t), 0\bigr)$
- $\vec L(t) = \bigl(0, 0, mR^2\omega\bigr)$
- $|\vec L| = mR^2\omega$ (constant)
- $\vec \tau = \vec 0$
- $\frac{d\vec L}{dt} = \vec 0$

## Interpretation

In uniform circular motion, the angular momentum is conserved because there is no net torque acting on the system. The force responsible for the motion (centripetal force) acts purely parallel to the position vector, and central forces do not generate torque. This is a foundational principle underlying planetary motion and Kepler's Second Law.