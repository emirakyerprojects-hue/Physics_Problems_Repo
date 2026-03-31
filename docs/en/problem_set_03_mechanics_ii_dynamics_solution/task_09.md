# Task 09 – Potential and conservative field

## Problem Statement

Given the potential energy function in two dimensions:

$$
U(x,y) = \frac{k}{2}(x^2+y^2)
$$

Determine:
1. The force vector $\vec F$ as the negative gradient of the potential.
2. The equations of motion.
3. The type of motion exhibited by the system.
4. The total mechanical energy.
5. The geometric interpretation of the trajectory for an HTML/JS application.

## Theory

A conservative force field can be derived entirely from a scalar potential energy function using the gradient operator:

$$
\vec F = -\nabla U = \left( -\frac{\partial U}{\partial x}, -\frac{\partial U}{\partial y} \right)
$$

The total mechanical energy in a multi-dimensional conservative field is the sum of the translational kinetic energies in all spatial dimensions and the scalar potential energy.

## Step-by-Step Solution

### 1. Force vector

Compute the partial derivatives of $U(x,y)$:

$$
\frac{\partial U}{\partial x} = kx
$$

$$
\frac{\partial U}{\partial y} = ky
$$

The force vector is the negative gradient:

$$
\begin{align}
\vec F &= -(kx, ky) \\
       &= -k(x, y) \\
       &= -k\vec r
\end{align}
$$

### 2. Equations of motion

Apply Newton's second law ($\vec F = m\ddot{\vec r}$) to the individual components:

$$
m\ddot{x} = -kx
$$

$$
m\ddot{y} = -ky
$$

### 3. Type of motion

The equations of motion represent two independent, uncoupled simple harmonic oscillators with the identical natural frequency $\omega_0 = \sqrt{k/m}$.

The general solutions are:

$$
x(t) = A_x \cos(\omega_0 t + \phi_x)
$$

$$
y(t) = A_y \cos(\omega_0 t + \phi_y)
$$

This describes an isotropic two-dimensional harmonic oscillator. Depending on the phase difference $\Delta\phi = \phi_y - \phi_x$ and amplitudes, the motion traces out a Lissajous figure that is strictly restricted to an ellipse, a circle, or a straight line segment.

### 4. Total mechanical energy

The total energy is the sum of the kinetic and potential energies:

$$
\begin{align}
E &= T + U \\
  &= \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2)
\end{align}
$$

Because the forces are strictly conservative, $E$ remains constant throughout the motion.

### 5. Geometric interpretation for visualization

To visualize the trajectory in an HTML/JS canvas:
- The force always points strictly toward the origin $(0,0)$ and its magnitude increases linearly with distance. This defines a central restoring force.
- The path $(x(t), y(t))$ traces a closed elliptical orbit centered exactly on the origin.
- The energy contours defined by $U(x,y) = \text{const}$ form concentric circles. The particle is bounded within the region where $U(x,y) \le E$.

## Final Result

- $\vec F = -k\vec r$
- $m\ddot{x} = -kx$ and $m\ddot{y} = -ky$
- The motion is an isotropic 2D harmonic oscillator (elliptical orbit).
- $E = \frac{1}{2}m(\dot{x}^2 + \dot{y}^2) + \frac{k}{2}(x^2 + y^2)$

## Interpretation

The isotropic quadratic potential well models a particle attached to the origin by a spring that obeys Hooke's Law in all directions. Because the $x$ and $y$ motions are completely uncoupled, the problem reduces to two independent 1D problems, emphasizing the utility of selecting an orthogonal coordinate system.