# Task 09 – Chain of N springs (discrete wave model)

## Problem Statement

A system consists of $N$ masses connected by springs in a linear chain.

Determine:
1. The equations of motion for the discrete lattice.
2. The framework to solve the system numerically for large $N$.
3. The method to introduce a local initial disturbance.
4. The characteristics of pulse propagation.
5. The effect of $k$ and $m$ on the propagation speed, including an HTML animation design.

## Theory

A chain of $N$ identical coupled oscillators serves as a discrete mechanical model for wave propagation in continuous media (like a string or a crystal lattice). As $N \to \infty$, the discrete system approaches the continuous wave equation.

## Step-by-Step Solution

### 1. Equations of motion

Let $m$ be the mass of each particle, $k$ the spring constant, and $x_i$ the displacement of the $i$-th mass from its equilibrium position. 

Assuming fixed boundary conditions ($x_0 = 0$ and $x_{N+1} = 0$), the net force on the $i$-th mass depends on its displacement relative to its two immediate neighbors:

$$
m \ddot{x}_i = -k(x_i - x_{i-1}) - k(x_i - x_{i+1})
$$

$$
\ddot{x}_i = \frac{k}{m} (x_{i+1} - 2x_i + x_{i-1}) \quad \text{for } i = 1, 2, \dots, N
$$

This represents a system of $N$ coupled second-order differential equations.

### 2. Numerical solution framework

The system is transformed into $2N$ first-order differential equations:

$$
\frac{dx_i}{dt} = v_i
$$

$$
\frac{dv_i}{dt} = \frac{k}{m} (x_{i+1} - 2x_i + x_{i-1})
$$

Using an RK4 or a Verlet integration scheme, an array of positions `X` and velocities `V` is updated at each time step. The boundaries remain fixed (`X[0] = 0`, `X[N+1] = 0`).

### 3. Local initial disturbance

To simulate a pulse, the system starts at rest ($v_i = 0$ for all $i$), but a single mass or a small group of masses near one end is given a non-zero initial displacement (e.g., a Gaussian profile). Alternatively, a brief external driving force can be applied to the first mass.

### 4. Propagation of the pulse

When the simulation runs, the displaced mass exerts a force on its neighbor, which subsequently accelerates and pulls the next neighbor. The disturbance travels sequentially down the chain. 

When the pulse hits the fixed boundary at $x_{N+1}$, it undergoes a phase inversion and reflects back through the chain.

### 5. Effect of parameters on propagation speed

The speed of the wave pulse through the discrete chain is analogous to the speed of sound in a solid. 

In the continuum limit, substituting $x_i(t) = f(x,t)$ and performing a Taylor expansion yields the wave equation with propagation speed:

$$
v = a \sqrt{\frac{k}{m}}
$$

where $a$ is the equilibrium spacing between masses. 
- Increasing stiffness $k$ increases the restoring force, causing the medium to respond faster, raising the wave speed.
- Increasing inertia $m$ makes the particles more sluggish, lowering the wave speed.

## Final Result

- Equations of motion: $\ddot{x}_i = \frac{k}{m} (x_{i+1} - 2x_i + x_{i-1})$
- Propagation speed relationship: $v \propto \sqrt{\frac{k}{m}}$

## Interpretation

The 1D chain fundamentally illustrates how local neighbor-to-neighbor interactions facilitate long-range energy transport without the macroscopic transport of matter. The discrete nature of the lattice also introduces dispersion (high-frequency ripples travel at different speeds than low-frequency envelopes), a phenomenon not captured by the continuous, ideal wave equation.