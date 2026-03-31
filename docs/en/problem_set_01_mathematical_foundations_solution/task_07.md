# Task 07 – Work of a force along a trajectory

## Problem Statement

Given a force field and a parametric trajectory:

$$
\vec F(x,y) = (y, 2x)
$$

$$
x = t, \qquad y = t^2, \qquad t \in [0,1]
$$

Determine:
1. The velocity vector $\vec v(t)$.
2. The work done by the force $\vec F$ along the trajectory.
3. The expression of the work integral as the limit of a Riemann sum for numerical computation.

## Theory

The mechanical work done by a force $\vec F$ on a particle moving along a curve $C$ is given by the line integral of the force along that path:

$$
W = \int_C \vec F \cdot d\vec r
$$

By parameterizing the path with time $t$, the differential displacement becomes $d\vec r = \vec v(t) dt$, transforming the line integral into a standard definite integral:

$$
W = \int_{t_0}^{t_1} \vec F(\vec r(t)) \cdot \vec v(t) \, dt
$$

A definite integral can be approximated numerically or rigorously defined as the limit of a Riemann sum as the number of partitions $N$ approaches infinity.

## Step-by-Step Solution

### 1. Velocity vector

Differentiating the position components with respect to $t$:

$$
\begin{align}
\vec v(t) &= \left( \frac{dx}{dt}, \frac{dy}{dt} \right) \\
          &= (1, 2t)
\end{align}
$$

### 2. Work done by the force

First, express the force vector along the specific trajectory by substituting $x(t)$ and $y(t)$ into $\vec F(x,y)$:

$$
\begin{align}
\vec F(\vec r(t)) &= (y(t), 2x(t)) \\
                  &= (t^2, 2t)
\end{align}
$$

Next, compute the dot product of the force and velocity vectors:

$$
\begin{align}
\vec F(\vec r(t)) \cdot \vec v(t) &= (t^2)(1) + (2t)(2t) \\
                                  &= t^2 + 4t^2 \\
                                  &= 5t^2
\end{align}
$$

Integrate this result over the given time interval $t \in [0,1]$:

$$
\begin{align}
W &= \int_0^1 5t^2 \, dt \\
  &= \left[ \frac{5}{3}t^3 \right]_0^1 \\
  &= \frac{5}{3}(1)^3 - \frac{5}{3}(0)^3 \\
  &= \frac{5}{3}
\end{align}
$$

### 3. Riemann sum formulation

To evaluate this integral numerically, partition the interval $[0,1]$ into $N$ equal subintervals of width $\Delta t = 1/N$. Let $t_i = i\Delta t$ be the right endpoint of the $i$-th subinterval.

The work is approximated by the Riemann sum:

$$
W \approx \sum_{i=1}^N \left( 5t_i^2 \right) \Delta t
$$

The exact value is the limit as $N \to \infty$:

$$
W = \lim_{N \to \infty} \sum_{i=1}^N 5 \left(\frac{i}{N}\right)^2 \frac{1}{N}
$$

## Final Result

- $\vec v(t) = (1, 2t)$
- $W = \frac{5}{3}$
- $W = \lim_{N \to \infty} \sum_{i=1}^N 5 \left(\frac{i}{N}\right)^2 \frac{1}{N}$

## Interpretation

The positive value of the work integral implies that the force field transfers energy to the particle as it moves along the parabolic path. Transforming a line integral into a definite integral with respect to time reduces a multidimensional spatial problem into a strictly one-dimensional calculation.