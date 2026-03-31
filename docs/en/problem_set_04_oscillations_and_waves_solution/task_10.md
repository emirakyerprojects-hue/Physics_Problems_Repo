# Task 10 – Double pendulum and deterministic chaos

## Problem Statement

Perform a purely numerical analysis of a double pendulum to visualize deterministic chaos.

Determine:
1. The Cartesian coordinates $(x_1,y_1)$ and $(x_2,y_2)$ as functions of the angles $(\theta_1,\theta_2)$.
2. The numerical integration framework (RK4) and stability checks.
3. The method to simulate 50 simultaneous copies demonstrating sensitivity to initial conditions.
4. The behavior of trajectory divergence across different perturbation scales, culminating in an HTML "ensemble" visualization.

## Theory

A double pendulum is a classic example of a complex dynamical system exhibiting deterministic chaos. Despite being governed by exact, deterministic Newtonian mechanics, its extreme sensitivity to initial conditions (the "butterfly effect") renders long-term prediction computationally impossible.

## Step-by-Step Solution

### 1. Cartesian coordinate transformations

Let $\theta_1$ and $\theta_2$ be the angles of the first and second rods measured from the downward vertical. Let the pivot of the first pendulum be at the origin $(0,0)$.

The coordinates of the first mass $m_1$ are:

$$
x_1 = l_1 \sin\theta_1
$$

$$
y_1 = -l_1 \cos\theta_1
$$

The coordinates of the second mass $m_2$ are measured relative to the first mass:

$$
x_2 = x_1 + l_2 \sin\theta_2
$$

$$
y_2 = y_1 - l_2 \cos\theta_2
$$

### 2. Numerical integration and stability

The non-linear equations of motion for $\ddot{\theta}_1$ and $\ddot{\theta}_2$ (derived from Lagrangian mechanics) are highly coupled. 
Let the state vector be $\vec{S} = [\theta_1, \omega_1, \theta_2, \omega_2]$. 

Using the 4th-order Runge-Kutta (RK4) algorithm, the state is iteratively advanced by a small time step $\Delta t \le 0.01\ \mathrm{s}$. 

**Stability Check:** The total mechanical energy of an undamped double pendulum must be conserved. Calculating $E = T + U$ at each time step verifies stability. If $\Delta t$ is too large, energy will artificially drift, indicating numerical instability.

### 3. Sensitivity to initial conditions (Ensemble Simulation)

Define a base initial state, e.g., $\vec{S}_0 = [\pi/2, 0, \pi/2, 0]$. 

Create an array of 50 independent pendulum objects. Initialize each with a minutely altered state. For instance, add a tiny random perturbation $\epsilon$ to the initial angle of the second rod:

$$
\theta_{2,i}(0) = \theta_{2,base} + \epsilon_i
$$

where $\epsilon_i$ is distributed uniformly between $-10^{-4}$ and $10^{-4}$ radians.

During the simulation, iterate the RK4 step for all 50 pendulums simultaneously.

### 4. Divergence and observation

In the initial phase of the simulation, all 50 pendulums appear to move as a single, thick line. Because the system is locally predictable, the tiny differences in starting angles only cause microscopic deviations.

As the chaotic regime unfolds (often after the first "flip" of the second pendulum), the distance between states in phase space grows exponentially, characterized by a positive Lyapunov exponent. The single visual trace rapidly frays into 50 entirely independent, unpredictable paths. 

Scaling the perturbation determines the onset time of visible divergence. A perturbation of $10^{-2}$ will separate almost instantly, whereas $10^{-6}$ will remain coherent for slightly longer before inevitably succumbing to chaos.

## Final Result

- $x_1 = l_1 \sin\theta_1$, $y_1 = -l_1 \cos\theta_1$
- $x_2 = l_1 \sin\theta_1 + l_2 \sin\theta_2$, $y_2 = -l_1 \cos\theta_1 - l_2 \cos\theta_2$
- The system demonstrates strict positive Lyapunov exponent divergence.

## Interpretation

The double pendulum fundamentally breaks the classical intuition that "similar causes yield similar effects." An interactive ensemble visualization using distinct colors perfectly encapsulates this: what begins as an ordered, identical set of machines flawlessly executing Newtonian laws explodes into a mesmerizing, chaotic cloud, proving that determinism does not guarantee predictability.