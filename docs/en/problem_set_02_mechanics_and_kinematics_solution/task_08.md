# Task 08 – Relative motion

## Problem Statement

Body A moves with velocity $\vec v_A = (3, 1)$, and body B moves with velocity $\vec v_B = (1, -2)$.

Determine:
1. The relative velocity $\vec v_{A/B}$.
2. The direction of the relative motion.
3. The conceptual setup for visualizing the motion of both bodies in three different reference frames: the laboratory frame, the frame of A, and the frame of B.

## Theory

The relative velocity of an object A with respect to an object B is the vector difference of their absolute velocities measured in a common inertial reference frame (typically the laboratory frame).

$$
\vec v_{A/B} = \vec v_A - \vec v_B
$$

The direction of a 2D vector $\vec v = (v_x, v_y)$ is given by the angle $\theta$ relative to the positive x-axis, calculated using the arctangent function.

## Step-by-Step Solution

### 1. Relative velocity

Subtract the velocity vector of body B from the velocity vector of body A:

$$
\begin{align}
\vec v_{A/B} &= (3, 1) - (1, -2) \\
             &= (3 - 1, 1 - (-2)) \\
             &= (2, 3)
\end{align}
$$

### 2. Direction of relative motion

Calculate the angle $\theta$ of the vector $\vec v_{A/B} = (2, 3)$ with respect to the horizontal axis:

$$
\tan\theta = \frac{v_{y, A/B}}{v_{x, A/B}} = \frac{3}{2}
$$

$$
\theta = \arctan(1.5)
$$

This corresponds to approximately $56.3^\circ$ above the positive x-axis.

### 3. Visualization in different reference frames

**Laboratory Frame (origin fixed):**
Both bodies move along straight lines determined by their absolute velocities. Assuming they start at the origin at $t=0$:
- Trajectory of A: $\vec r_A(t) = (3t, t)$
- Trajectory of B: $\vec r_B(t) = (t, -2t)$

**Reference Frame attached to Body A:**
Body A is stationary at the origin of this frame. Body B moves backward relative to A.
- Velocity of B relative to A: $\vec v_{B/A} = \vec v_B - \vec v_A = (-2, -3)$
- Trajectory of B: $\vec r_{B/A}(t) = (-2t, -3t)$

**Reference Frame attached to Body B:**
Body B is stationary at the origin of this frame. Body A moves with the calculated relative velocity.
- Velocity of A relative to B: $\vec v_{A/B} = (2, 3)$
- Trajectory of A: $\vec r_{A/B}(t) = (2t, 3t)$

## Final Result

- $\vec v_{A/B} = (2, 3)$
- Direction: $\theta = \arctan(1.5) \approx 56.3^\circ$

## Interpretation

Transforming between Galilean reference frames simplifies the analysis of multiple moving bodies. In the frame of a moving observer, the entire rest of the universe receives an added velocity component equal and opposite to the observer's absolute velocity.