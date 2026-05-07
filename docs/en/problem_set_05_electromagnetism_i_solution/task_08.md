# Task 08 – Energy of a three-charge system

## Problem Statement

1. Write the total energy of the system.
2. Calculate the energy for an equilateral triangle configuration.
3. Investigate the change in energy when changing the sign of one charge.
4. Find the minimum energy configuration (numerically/conceptually).
5. Interpret the stability of the system.

## Theory

The total electrostatic potential energy $U$ of a system of discrete point charges is the work required to assemble the system by bringing the charges from infinity to their final positions. It is calculated as the sum of the pairwise interaction energies:

$$
U = \sum_{i < j} k \frac{q_i q_j}{r_{ij}}
$$

where $k$ is Coulomb's constant, $q_i$ and $q_j$ are the magnitudes of the charges, and $r_{ij}$ is the distance between the $i$-th and $j$-th charges.

## Step-by-Step Solution

### 1. Total energy of the three-charge system

For a system of three charges ($q_1, q_2, q_3$), the total potential energy equation expands to three interaction pairs:

$$
U = k \left( \frac{q_1 q_2}{r_{12}} + \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)
$$

### 2. Energy for an equilateral triangle configuration

Assume three identical charges $q_1 = q_2 = q_3 = q$ arranged at the vertices of an equilateral triangle with side length $a$. The distances are equal: $r_{12} = r_{13} = r_{23} = a$.

Substituting these values into the energy equation:

$$
\begin{align}
U_{\text{eq}} &= k \left( \frac{q \cdot q}{a} + \frac{q \cdot q}{a} + \frac{q \cdot q}{a} \right) \\
              &= 3k \frac{q^2}{a}
\end{align}
$$

### 3. Change in energy when changing the sign of one charge

If the sign of one charge (e.g., $q_3$) is inverted such that $q_1 = q, q_2 = q, q_3 = -q$, the energy equation becomes:

$$
\begin{align}
U_{\text{new}} &= k \left( \frac{q \cdot q}{a} + \frac{q \cdot (-q)}{a} + \frac{q \cdot (-q)}{a} \right) \\
               &= k \left( \frac{q^2}{a} - \frac{q^2}{a} - \frac{q^2}{a} \right) \\
               &= -k \frac{q^2}{a}
\end{align}
$$

The energy transitions from a highly positive (repulsive) state to a negative (bound) state.

### 4. Minimum energy configuration

Finding the minimum energy configuration numerically involves treating $U(x_1, y_1, x_2, y_2, x_3, y_3)$ as an objective function and applying a gradient descent algorithm. The gradient of the energy corresponds to the negative of the electrostatic forces acting on the charges. 

If three positive charges are free to move in an unbounded space, the force is purely repulsive, and the system minimizes energy by expanding to infinity ($U \to 0$).

If the charges are constrained (e.g., forced to remain on a circle of radius $R$), the numerical minimization pushes the charges as far apart as possible. For three identical charges, the minimum energy configuration on a circle is precisely the equilateral triangle. If the system consists of two positive charges and one negative charge, the minimum energy configuration places the negative charge directly between the two positive charges on a straight line.

### 5. Interpretation of system stability

The total potential energy is a direct indicator of system stability. A highly positive potential energy indicates an unstable, forced assembly; the charges will fly apart if released. A negative potential energy indicates a bound state where external work must be supplied to dismantle the system. However, as dictated by Earnshaw's Theorem, no purely electrostatic configuration of discrete charges is entirely stable against all perturbations; an equilibrium point in one dimension will invariably be an unstable saddle point in another.

## Final Result

1. $U = k \left( \frac{q_1 q_2}{r_{12}} + \frac{q_1 q_3}{r_{13}} + \frac{q_2 q_3}{r_{23}} \right)$
2. $U_{\text{eq}} = 3k \frac{q^2}{a}$
3. $U_{\text{new}} = -k \frac{q^2}{a}$
4. Unconstrained minimum energy is at infinite separation; constrained minima form symmetric geometric arrangements.
5. Systems with $U < 0$ are globally bound, but locally unstable to certain spatial perturbations.