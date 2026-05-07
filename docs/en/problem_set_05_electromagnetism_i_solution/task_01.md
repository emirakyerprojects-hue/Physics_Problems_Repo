# Task 01 – Potential and Energy

## Problem Statement

For a point charge $q = 4 \ \mu\mathrm{C}$:
1. Calculate the potential at $r_1 = 0.3 \ \mathrm{m}$.
2. Calculate the potential difference between $r_1 = 0.3 \ \mathrm{m}$ and $r_2 = 0.6 \ \mathrm{m}$.
3. Calculate the work done to move a test charge $q_0 = 2 \ \mu\mathrm{C}$ from $r_1$ to $r_2$.
4. Calculate the electric field intensity from the derivative of the potential.
5. Compare with Coulomb's law.

## Theory

The electric potential $V(r)$ at a distance $r$ from a point charge $q$ is defined as the potential energy per unit charge and is given by:

$$
V(r) = \frac{1}{4\pi\varepsilon_0} \frac{q}{r} = k \frac{q}{r}
$$

where $k \approx 9 \times 10^9 \ \mathrm{N \cdot m^2 / C^2}$ is Coulomb's constant.

The potential difference $\Delta V$ between two points is the change in potential:

$$
\Delta V = V(r_2) - V(r_1)
$$

The work $W$ required by an external agent to move a test charge $q_0$ through a potential difference $\Delta V$ at a constant velocity is:

$$
W = q_0 \Delta V
$$

The electric field $\vec{E}$ is the negative gradient of the electric potential. For a spherically symmetric potential, the radial component of the electric field is:

$$
E_r = -\frac{dV}{dr}
$$

## Step-by-Step Solution

### 1. Potential at $r_1 = 0.3 \ \mathrm{m}$

Substituting the given values into the potential formula:

$$
\begin{align}
V_1 &= \left( 9 \times 10^9 \right) \frac{4 \times 10^{-6}}{0.3} \\
    &= \frac{36 \times 10^3}{0.3} \\
    &= 120 \times 10^3 \ \mathrm{V}
\end{align}
$$

$$
V_1 = 120 \ \mathrm{kV}
$$

### 2. Potential difference between $r_1$ and $r_2$

First, calculate the potential at $r_2 = 0.6 \ \mathrm{m}$:

$$
\begin{align}
V_2 &= \left( 9 \times 10^9 \right) \frac{4 \times 10^{-6}}{0.6} \\
    &= 60 \times 10^3 \ \mathrm{V}
\end{align}
$$

The potential difference is:

$$
\begin{align}
\Delta V &= V_2 - V_1 \\
         &= 60 \ \mathrm{kV} - 120 \ \mathrm{kV} \\
         &= -60 \ \mathrm{kV}
\end{align}
$$

### 3. Work done to move a test charge

The external work done to move the test charge $q_0 = 2 \ \mu\mathrm{C}$ from $r_1$ to $r_2$ is:

$$
\begin{align}
W &= q_0 \Delta V \\
  &= \left( 2 \times 10^{-6} \right) \left( -60 \times 10^3 \right) \\
  &= -0.12 \ \mathrm{J}
\end{align}
$$

### 4. Electric field from the derivative of the potential

Taking the derivative of the generic potential function $V(r)$ with respect to $r$:

$$
\begin{align}
E_r &= -\frac{d}{dr} \left( k \frac{q}{r} \right) \\
    &= -k q \frac{d}{dr} \left( r^{-1} \right) \\
    &= -k q \left( -r^{-2} \right) \\
    &= k \frac{q}{r^2}
\end{align}
$$

### 5. Comparison with Coulomb's law

Coulomb's law states that the electrostatic force $F$ between a source charge $q$ and a test charge $q_0$ is:

$$
F = k \frac{q q_0}{r^2}
$$

The magnitude of the electric field $E$ is defined as the force per unit charge:

$$
\begin{align}
E &= \frac{F}{q_0} \\
  &= k \frac{q}{r^2}
\end{align}
$$

## Final Result

1. $V(0.3 \ \mathrm{m}) = 120 \ \mathrm{kV}$
2. $\Delta V = -60 \ \mathrm{kV}$
3. $W = -0.12 \ \mathrm{J}$
4. $E_r = k \frac{q}{r^2}$
5. The derivative of the potential yields the exact formula defined by Coulomb's law.

## Interpretation

The electric potential decreases as the distance from the positive source charge increases. Consequently, moving a positive test charge further away (from $0.3 \ \mathrm{m}$ to $0.6 \ \mathrm{m}$) results in a negative potential difference. The negative work calculated indicates that the electric field itself does positive work on the test charge. This means no external energy input is required to move the charge outward; rather, the system releases $0.12 \ \mathrm{J}$ of potential energy. The perfect agreement between the gradient of the potential and Coulomb's law confirms the fundamental relationship between electrostatic force and electric potential energy.