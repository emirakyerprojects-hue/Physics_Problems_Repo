# Task 08 – Two coupled springs (two degrees of freedom)

## Problem Statement

Two masses ($m_1, m_2$) are connected to walls in a series configuration by three springs with constants $k_1$, $k_2$, and $k_3$.

Determine:
1. The equations of motion for both masses.
2. The method to determine natural frequencies.
3. The method to find normal modes.
4. The numerical solution for arbitrary initial conditions.
5. The energy exchange mechanism between the masses.

## Theory

A system of multiple connected masses exhibits coupled differential equations. The motion of one mass directly influences the forces acting on the other. 

Such a system can be decomposed into independent harmonic oscillators known as normal modes. Each mode oscillates at a specific natural frequency, and any arbitrary motion of the system is a linear superposition of these normal modes.

## Step-by-Step Solution

### 1. Equations of motion

Let $x_1$ and $x_2$ be the displacements of $m_1$ and $m_2$ from their respective equilibrium positions.

- Mass 1 is connected to the left wall by $k_1$ and to Mass 2 by $k_2$.
- Mass 2 is connected to Mass 1 by $k_2$ and to the right wall by $k_3$.

Apply Newton's second law:

$$
m_1 \ddot{x}_1 = -k_1 x_1 + k_2 (x_2 - x_1)
$$

$$
m_2 \ddot{x}_2 = -k_2 (x_2 - x_1) - k_3 x_2
$$

Rearranging into matrix form $M\ddot{\vec{x}} = -K\vec{x}$:

$$
\begin{pmatrix} m_1 & 0 \\ 0 & m_2 \end{pmatrix} 
\begin{pmatrix} \ddot{x}_1 \\ \ddot{x}_2 \end{pmatrix} 
= -
\begin{pmatrix} k_1 + k_2 & -k_2 \\ -k_2 & k_2 + k_3 \end{pmatrix}
\begin{pmatrix} x_1 \\ x_2 \end{pmatrix}
$$

### 2. Natural frequencies

Assume a harmonic solution of the form $\vec{x}(t) = \vec{A} e^{i\omega t}$. Substituting this into the matrix equation yields an eigenvalue problem:

$$
(-M \omega^2 + K) \vec{A} = \vec{0}
$$

For non-trivial solutions ($\vec{A} \neq \vec{0}$), the determinant of the coefficient matrix must be zero:

$$
\det(K - \omega^2 M) = 0
$$

$$
\det \begin{pmatrix} k_1 + k_2 - m_1 \omega^2 & -k_2 \\ -k_2 & k_2 + k_3 - m_2 \omega^2 \end{pmatrix} = 0
$$

This produces a quadratic equation in $\omega^2$ (the characteristic equation):

$$
(k_1 + k_2 - m_1 \omega^2)(k_2 + k_3 - m_2 \omega^2) - k_2^2 = 0
$$

Solving this yields two positive roots, $\omega_1^2$ and $\omega_2^2$, which are the squares of the natural frequencies.

### 3. Normal modes

For each natural frequency $\omega_i$, substitute it back into the eigenvalue equation to find the corresponding eigenvector $\vec{A}_i = (A_{1i}, A_{2i})^T$. This vector dictates the relative amplitudes and phases of the masses in that specific mode.

- **Symmetric mode (lower frequency):** The masses generally move in the same direction.
- **Antisymmetric mode (higher frequency):** The masses move in opposite directions, maximally compressing the middle spring $k_2$.

### 4. Numerical solution

Convert to a system of four first-order ODEs:

$$
\frac{dx_1}{dt} = v_1, \qquad \frac{dv_1}{dt} = \frac{-k_1 x_1 + k_2 (x_2 - x_1)}{m_1}
$$

$$
\frac{dx_2}{dt} = v_2, \qquad \frac{dv_2}{dt} = \frac{-k_2 (x_2 - x_1) - k_3 x_2}{m_2}
$$

Use an integrator like RK4 to compute the state vector $[x_1, v_1, x_2, v_2]$ over discrete time steps.

### 5. Energy exchange

The total mechanical energy $E_{tot} = K_1 + K_2 + U_1 + U_2 + U_{12}$ is conserved. If the system is started with only Mass 1 displaced, the energy will gradually transfer through the coupling spring $k_2$ into Mass 2. Mass 1 will temporarily come to rest as Mass 2 reaches maximum amplitude, and the cycle will reverse. This defines the phenomenon of beats in coupled oscillators.

## Final Result

- Matrix Equation: $M\ddot{\vec{x}} = -K\vec{x}$
- Characteristic equation: $(k_1 + k_2 - m_1 \omega^2)(k_2 + k_3 - m_2 \omega^2) - k_2^2 = 0$
- The system exhibits two distinct natural frequencies and normal modes.

## Interpretation

Coupling creates an interaction channel between degrees of freedom. The stiffness of the middle spring ($k_2$) dictates the coupling strength. Weak coupling leads to a slow, near-complete transfer of energy between the masses, observable visually as a beating pattern in the envelope of each mass's trajectory.