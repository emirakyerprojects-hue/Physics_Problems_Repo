# Task 09 – Change of reference frame (Copernican model to geocentric description)

## Problem Statement

Earth and Mars move in circular orbits around the Sun in the heliocentric system:

$$
\vec r_Z(t) = R_Z \bigl(\cos(\omega_Z t), \sin(\omega_Z t)\bigr)
$$

$$
\vec r_M(t) = R_M \bigl(\cos(\omega_M t), \sin(\omega_M t)\bigr)
$$

Determine:
1. The mathematical form of the motions in the heliocentric system.
2. The position of Mars relative to Earth in the geocentric system, $\vec r_{M/Z}(t)$.
3. The explicit components $x_{M/Z}(t)$ and $y_{M/Z}(t)$.
4. The setup for an HTML animation comparing the two systems.

## Theory

In the heliocentric (Sun-centered) model, planets follow approximately circular, independent orbits parameterized by their respective orbital radii and angular frequencies. 

To convert this to a geocentric (Earth-centered) model, a vector translation is performed. The coordinate system is shifted such that the Earth always resides at the origin. This requires subtracting the Earth's position vector from the position vector of any other celestial body.

## Step-by-Step Solution

### 1. Heliocentric motion

Both trajectories $\vec r_Z(t)$ and $\vec r_M(t)$ represent circles centered at the origin $(0,0)$ with radii $R_Z$ and $R_M$. Since they orbit the Sun in the same direction, both angular velocities $\omega_Z$ and $\omega_M$ share the same sign (typically positive for counter-clockwise rotation).

### 2. Relative position vector

The position of Mars as measured from Earth is the vector difference:

$$
\vec r_{M/Z}(t) = \vec r_M(t) - \vec r_Z(t)
$$

Substitute the parametric definitions:

$$
\vec r_{M/Z}(t) = R_M \bigl(\cos(\omega_M t), \sin(\omega_M t)\bigr) - R_Z \bigl(\cos(\omega_Z t), \sin(\omega_Z t)\bigr)
$$

### 3. Explicit components

Separate the vector equation into orthogonal scalar components:

$$
x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)
$$

$$
y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)
$$

### 4. Animation Setup

- **Panel A (Heliocentric):** The origin $(0,0)$ remains fixed on the Sun. Draw two concentric circles. A point representing Earth revolves on the inner circle (since $R_Z < R_M$) with a faster angular velocity ($\omega_Z > \omega_M$). A point representing Mars revolves on the outer circle.
- **Panel B (Geocentric):** The origin $(0,0)$ remains fixed on the Earth. Plot the trace of the curve defined by $(x_{M/Z}(t), y_{M/Z}(t))$. Because the angular velocities differ, this parametric curve traces out an epicycloid-like path characterized by retrograde loops when Earth overtakes Mars in its orbit.

## Final Result

- $\vec r_{M/Z}(t) = \bigl( R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t), \, R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t) \bigr)$
- $x_{M/Z}(t) = R_M \cos(\omega_M t) - R_Z \cos(\omega_Z t)$
- $y_{M/Z}(t) = R_M \sin(\omega_M t) - R_Z \sin(\omega_Z t)$

## Interpretation

This mathematical transformation demonstrates why ancient astronomers, observing from a geocentric perspective, had to introduce complex systems of epicycles to model the paths of the planets. The retrograde loops are entirely explained as an artifact of observing a slower-moving outer body from a faster-moving inner body on nested circular orbits.