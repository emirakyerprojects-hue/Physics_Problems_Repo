# Task 03 – Work of a variable force

## Problem Statement

Given a one-dimensional force:

$$
F(x) = -kx
$$

Determine:
1. The equation of motion and its solution.
2. The work done during the displacement from $0$ to $x_0$.
3. The interpretation of the result as potential energy.
4. The verification of the relationship $F = -\frac{dU}{dx}$.
5. The framework for graphing $F(x)$ and $U(x)$.

## Theory

A force proportional to the negative of displacement defines an ideal spring or a linear restoring force (Hooke's Law), causing simple harmonic motion.

The work done by a variable force in one dimension is defined by the definite integral:

$$
W = \int_{x_i}^{x_f} F(x) \, dx
$$

For a conservative force, the work done by the field is equal to the negative change in potential energy:

$$
W = -\Delta U = -(U_f - U_i)
$$

This directly implies the local differential relationship:

$$
F(x) = -\frac{dU}{dx}
$$

## Step-by-Step Solution

### 1. Equation of motion and solution

Using Newton's second law ($F = ma$ and $a = \frac{d^2x}{dt^2}$):

$$
m \frac{d^2x}{dt^2} = -kx
$$

Rearranging into the standard form of a second-order linear homogeneous differential equation:

$$
\frac{d^2x}{dt^2} + \frac{k}{m} x = 0
$$

Let $\omega^2 = \frac{k}{m}$. The equation becomes:

$$
\ddot{x} + \omega^2 x = 0
$$

The general solution represents harmonic oscillation:

$$
x(t) = A \cos(\omega t) + B \sin(\omega t)
$$

where $A$ and $B$ are constants determined by initial conditions.

### 2. Work done

Integrate the force function from $x = 0$ to $x = x_0$:

$$
\begin{align}
W &= \int_{0}^{x_0} (-kx) \, dx \\
  &= \left[ -\frac{1}{2}kx^2 \right]_0^{x_0} \\
  &= -\frac{1}{2}k x_0^2 - (-0) \\
  &= -\frac{1}{2}k x_0^2
\end{align}
$$

### 3. Potential energy interpretation

By definition, the change in potential energy equals the negative work done by the conservative force:

$$
\Delta U = -W
$$

$$
U(x_0) - U(0) = \frac{1}{2}k x_0^2
$$

Setting the reference point for potential energy such that $U(0) = 0$ at the equilibrium position:

$$
U(x_0) = \frac{1}{2}k x_0^2
$$

Generalizing for any position $x$:

$$
U(x) = \frac{1}{2}kx^2
$$

### 4. Verification of the derivative relationship

Take the derivative of the derived potential energy function with respect to $x$:

$$
\begin{align}
-\frac{dU}{dx} &= -\frac{d}{dx} \left( \frac{1}{2}kx^2 \right) \\
               &= -\frac{1}{2}k (2x) \\
               &= -kx
\end{align}
$$

This precisely yields the original force function $F(x)$, verifying the fundamental relationship.

### 5. Graphing framework

- **$F(x)$ graph:** A straight line passing through the origin with a negative slope equal to $-k$. This signifies that a positive displacement causes a negative (restoring) force.
- **$U(x)$ graph:** An upward-opening parabola with its vertex at the origin $(0,0)$. The steepness of the parabola is determined by the stiffness constant $k$. 

## Final Result

- Equation of motion: $\ddot{x} + \omega^2 x = 0$
- Solution: $x(t) = A \cos(\omega t) + B \sin(\omega t)$
- $W = -\frac{1}{2}k x_0^2$
- $U(x) = \frac{1}{2}kx^2$
- Verified: $-\frac{dU}{dx} = -kx = F(x)$

## Interpretation

The linear restoring force performs negative work as the particle moves away from equilibrium, transferring kinetic energy into the potential energy of the field. The parabolic potential energy well geometrically demonstrates that the restoring force is steepest where the potential energy gradient is steepest.