# Task 09 – Dipole in an external field

## Problem Statement

A dipole in a uniform field $E_0$.
1. Derive the formula for the torque acting on the dipole.
2. Calculate the potential energy of the dipole.
3. Determine the equation of angular motion.
4. Linearize the equation for small displacements.
5. Interpret the system as a harmonic oscillator.

## Theory

An electric dipole consists of two equal and opposite point charges, $+q$ and $-q$, separated by a distance vector $\vec{d}$ pointing from the negative to the positive charge. The dipole moment is defined as:

$$
\vec{p} = q\vec{d}
$$

When placed in a uniform external electric field $\vec{E}_0$, the positive charge experiences a force $\vec{F}_+ = q\vec{E}_0$ and the negative charge experiences $\vec{F}_- = -q\vec{E}_0$. The net force is zero, but the forces generate a torque.

## Step-by-Step Solution

### 1. Torque acting on the dipole

The total torque $\vec{\tau}$ is the sum of the torques exerted on each charge relative to the center of mass. Assuming the center of mass is midway between the charges:

$$
\begin{align}
\vec{\tau} &= \left(\frac{\vec{d}}{2} \times \vec{F}_+\right) + \left(-\frac{\vec{d}}{2} \times \vec{F}_-\right) \\
           &= \left(\frac{\vec{d}}{2} \times q\vec{E}_0\right) + \left(-\frac{\vec{d}}{2} \times -q\vec{E}_0\right) \\
           &= q\vec{d} \times \vec{E}_0 \\
           &= \vec{p} \times \vec{E}_0
\end{align}
$$

The magnitude of the torque is $\tau = pE_0 \sin\theta$, where $\theta$ is the angle between the dipole moment and the electric field.

### 2. Potential energy of the dipole

The potential energy $U$ is defined as the work done to rotate the dipole from an orientation $\theta = \pi/2$ (chosen as the zero-energy reference point) to an angle $\theta$:

$$
\begin{align}
U &= -\int_{\pi/2}^{\theta} \tau \, d\theta' \\
  &= -\int_{\pi/2}^{\theta} \left(-pE_0 \sin\theta'\right) \, d\theta' \\
  &= -pE_0 \cos\theta \\
  &= -\vec{p} \cdot \vec{E}_0
\end{align}
$$

*(Note: The negative sign in the integral arises because the field exerts a restoring torque opposed to the increase in $\theta$.)*

### 3. Equation of angular motion

By Newton's second law for rotation, the net torque is equal to the moment of inertia $I$ times the angular acceleration $\alpha$:

$$
\tau_{\text{net}} = I \frac{d^2\theta}{dt^2}
$$

Substituting the restoring torque provided by the electric field ($\tau = -pE_0 \sin\theta$):

$$
I \frac{d^2\theta}{dt^2} = -pE_0 \sin\theta
$$

$$
\frac{d^2\theta}{dt^2} + \frac{pE_0}{I} \sin\theta = 0
$$

### 4. Linearization for small displacements

For small angular displacements ($\theta \ll 1 \ \mathrm{rad}$), the small-angle approximation states that $\sin\theta \approx \theta$. Applying this to the equation of motion yields the linearized differential equation:

$$
\frac{d^2\theta}{dt^2} + \frac{pE_0}{I} \theta = 0
$$

### 5. Interpretation as a harmonic oscillator

The linearized equation of motion has the exact mathematical form of a simple harmonic oscillator:

$$
\frac{d^2\theta}{dt^2} + \omega^2 \theta = 0
$$

where the angular frequency $\omega$ of the oscillation is:

$$
\omega = \sqrt{\frac{pE_0}{I}}
$$

This indicates that if the dipole is slightly displaced from alignment with the external electric field, it will not simply return to rest but will undergo periodic rotational oscillations around the equilibrium position ($\theta = 0$), analogous to a pendulum swinging in a gravitational field.

## Final Result

1. $\vec{\tau} = \vec{p} \times \vec{E}_0$
2. $U = -\vec{p} \cdot \vec{E}_0$
3. $\frac{d^2\theta}{dt^2} + \frac{pE_0}{I} \sin\theta = 0$
4. $\frac{d^2\theta}{dt^2} + \left(\frac{pE_0}{I}\right) \theta = 0$
5. The system exhibits simple harmonic motion with an oscillation period $T = 2\pi \sqrt{\frac{I}{pE_0}}$.