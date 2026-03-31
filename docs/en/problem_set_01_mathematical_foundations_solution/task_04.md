# Task 04 – Geometry of parametric curves

## Problem Statement

Investigate the following parametric curves:
A) $x(t) = R\cos t, \quad y(t) = R\sin t$
B) $x(t) = a\cos t, \quad y(t) = b\sin t$
C) $x(t) = t, \quad y(t) = t^2$
D) $x(t) = \cosh t, \quad y(t) = \sinh t$

For each curve, determine:
1. The equation with the parameter eliminated (if possible).
2. The type of curve.
3. The velocity $\vec v(t)$ and acceleration $\vec a(t)$.
4. Whether the velocity magnitude $|\vec v|$ or acceleration magnitude $|\vec a|$ is constant.

## Theory

Parametric equations define the coordinates of a particle as functions of an independent parameter, typically time $t$. Eliminating the parameter often requires the use of fundamental trigonometric identities, such as $\cos^2 t + \sin^2 t = 1$, or hyperbolic identities, such as $\cosh^2 t - \sinh^2 t = 1$. 

Kinematic quantities are obtained by successive time derivatives:

$$
\vec v(t) = \frac{d\vec r}{dt}
$$

$$
\vec a(t) = \frac{d\vec v}{dt}
$$

The magnitudes are computed using the Euclidean norm. If the derivative of a magnitude with respect to time is zero, the magnitude is constant.

## Step-by-Step Solution

### Curve A

**1. Eliminate the parameter:**

$$
\begin{align}
x^2 + y^2 &= (R\cos t)^2 + (R\sin t)^2 \\
          &= R^2(\cos^2 t + \sin^2 t) \\
          &= R^2
\end{align}
$$

**2. Type of curve:**
A circle of radius $R$ centered at the origin.

**3. Velocity and acceleration:**

$$
\vec v(t) = (-R\sin t, R\cos t)
$$

$$
\vec a(t) = (-R\cos t, -R\sin t)
$$

**4. Constant magnitudes:**

$$
\begin{align}
|\vec v(t)| &= \sqrt{(-R\sin t)^2 + (R\cos t)^2} \\
            &= \sqrt{R^2(\sin^2 t + \cos^2 t)} \\
            &= R
\end{align}
$$

$$
\begin{align}
|\vec a(t)| &= \sqrt{(-R\cos t)^2 + (-R\sin t)^2} \\
            &= R
\end{align}
$$

Both $|\vec v|$ and $|\vec a|$ are constant.

### Curve B

**1. Eliminate the parameter:**

$$
\begin{align}
\left(\frac{x}{a}\right)^2 + \left(\frac{y}{b}\right)^2 &= \cos^2 t + \sin^2 t \\
                                                        &= 1
\end{align}
$$

**2. Type of curve:**
An ellipse with semi-major and semi-minor axes $a$ and $b$.

**3. Velocity and acceleration:**

$$
\vec v(t) = (-a\sin t, b\cos t)
$$

$$
\vec a(t) = (-a\cos t, -b\sin t)
$$

**4. Constant magnitudes:**

$$
|\vec v(t)| = \sqrt{a^2\sin^2 t + b^2\cos^2 t}
$$

$$
|\vec a(t)| = \sqrt{a^2\cos^2 t + b^2\sin^2 t}
$$

Neither $|\vec v|$ nor $|\vec a|$ is constant (unless $a = b$, reducing to a circle).

### Curve C

**1. Eliminate the parameter:**
Substitute $t = x$ into the equation for $y$:

$$
y = x^2
$$

**2. Type of curve:**
A parabola opening upwards along the $y$-axis.

**3. Velocity and acceleration:**

$$
\vec v(t) = (1, 2t)
$$

$$
\vec a(t) = (0, 2)
$$

**4. Constant magnitudes:**

$$
|\vec v(t)| = \sqrt{1 + 4t^2}
$$

$$
|\vec a(t)| = \sqrt{0^2 + 2^2} = 2
$$

The magnitude $|\vec v|$ is not constant, but $|\vec a|$ is constant.

### Curve D

**1. Eliminate the parameter:**
Using the fundamental hyperbolic identity:

$$
\begin{align}
x^2 - y^2 &= \cosh^2 t - \sinh^2 t \\
          &= 1
\end{align}
$$

**2. Type of curve:**
The right branch of a unit hyperbola (since $x = \cosh t \ge 1$).

**3. Velocity and acceleration:**

$$
\vec v(t) = (\sinh t, \cosh t)
$$

$$
\vec a(t) = (\cosh t, \sinh t)
$$

**4. Constant magnitudes:**

$$
\begin{align}
|\vec v(t)| &= \sqrt{\sinh^2 t + \cosh^2 t} \\
            &= \sqrt{\cosh(2t)}
\end{align}
$$

$$
\begin{align}
|\vec a(t)| &= \sqrt{\cosh^2 t + \sinh^2 t} \\
            &= \sqrt{\cosh(2t)}
\end{align}
$$

Neither $|\vec v|$ nor $|\vec a|$ is constant.

## Final Result

- **Curve A:** Circle. $x^2+y^2=R^2$. Both $|\vec v|$ and $|\vec a|$ constant.
- **Curve B:** Ellipse. $(x/a)^2+(y/b)^2=1$. Neither constant.
- **Curve C:** Parabola. $y=x^2$. Only $|\vec a|$ is constant.
- **Curve D:** Hyperbola. $x^2-y^2=1$. Neither constant.

## Interpretation

Analyzing parametric forms enables the immediate determination of not only the spatial trajectory (the orbit) but also the time evolution of the system's kinematic state. A constant acceleration magnitude does not necessarily imply constant velocity magnitude, as demonstrated by the parabolic trajectory of projectile motion.