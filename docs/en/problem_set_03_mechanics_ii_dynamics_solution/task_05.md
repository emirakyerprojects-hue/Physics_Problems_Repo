# Task 05 – Momentum and one-dimensional head-on collision

## Problem Statement

Two bodies with masses $m_1$ and $m_2$ move along a single straight line and undergo an elastic collision. 

Determine:
1. The mathematical principles of conservation of momentum and energy.
2. The final velocities $u_1$ and $u_2$ after the collision given initial velocities $v_1$ and $v_2$.
3. The specific outcome for the case $m_1 = m_2$.
4. The specific outcome for the limit $m_2 \gg m_1$.
5. The physical interpretation of the results.

## Theory

An elastic collision is defined as a collision in which both total linear momentum and total kinetic energy are strictly conserved. 

The conservation of linear momentum states that the total momentum before the collision equals the total momentum after the collision.

The conservation of kinetic energy states that the total kinetic energy before the collision equals the total kinetic energy after the collision.

## Step-by-Step Solution

### 1. Conservation equations

Let $v_1, v_2$ be the initial velocities, and $u_1, u_2$ be the final velocities.

Conservation of momentum:

$$
m_1 v_1 + m_2 v_2 = m_1 u_1 + m_2 u_2
$$

Conservation of kinetic energy:

$$
\frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2 = \frac{1}{2}m_1 u_1^2 + \frac{1}{2}m_2 u_2^2
$$

### 2. Final velocities

Rearrange both equations to group terms by mass:

$$
m_1(v_1 - u_1) = m_2(u_2 - v_2)
$$

$$
m_1(v_1^2 - u_1^2) = m_2(u_2^2 - v_2^2)
$$

Factor the difference of squares in the energy equation:

$$
m_1(v_1 - u_1)(v_1 + u_1) = m_2(u_2 - v_2)(u_2 + v_2)
$$

Divide the factored energy equation by the rearranged momentum equation (assuming non-trivial collision $v_1 \neq u_1$):

$$
v_1 + u_1 = u_2 + v_2
$$

$$
u_2 = v_1 + u_1 - v_2
$$

Substitute this expression for $u_2$ back into the momentum equation:

$$
m_1 v_1 + m_2 v_2 = m_1 u_1 + m_2 (v_1 + u_1 - v_2)
$$

$$
m_1 v_1 + m_2 v_2 = m_1 u_1 + m_2 v_1 + m_2 u_1 - m_2 v_2
$$

Group terms with $u_1$:

$$
(m_1 - m_2) v_1 + 2m_2 v_2 = (m_1 + m_2) u_1
$$

$$
u_1 = \frac{m_1 - m_2}{m_1 + m_2} v_1 + \frac{2 m_2}{m_1 + m_2} v_2
$$

By symmetry, the velocity $u_2$ is:

$$
u_2 = \frac{2 m_1}{m_1 + m_2} v_1 + \frac{m_2 - m_1}{m_1 + m_2} v_2
$$

### 3. Case $m_1 = m_2$

Substitute $m_1 = m_2 = m$ into the final velocity equations:

$$
\begin{align}
u_1 &= \frac{0}{2m} v_1 + \frac{2m}{2m} v_2 \\
    &= v_2
\end{align}
$$

$$
\begin{align}
u_2 &= \frac{2m}{2m} v_1 + \frac{0}{2m} v_2 \\
    &= v_1
\end{align}
$$

### 4. Limit $m_2 \gg m_1$

Divide the numerator and denominator of the velocity equations by $m_2$ and take the limit as the ratio $\frac{m_1}{m_2} \to 0$:

$$
\begin{align}
u_1 &= \lim_{\frac{m_1}{m_2} \to 0} \left( \frac{\frac{m_1}{m_2} - 1}{\frac{m_1}{m_2} + 1} v_1 + \frac{2}{\frac{m_1}{m_2} + 1} v_2 \right) \\
    &= \frac{-1}{1} v_1 + \frac{2}{1} v_2 \\
    &= -v_1 + 2v_2
\end{align}
$$

$$
\begin{align}
u_2 &= \lim_{\frac{m_1}{m_2} \to 0} \left( \frac{2 \frac{m_1}{m_2}}{\frac{m_1}{m_2} + 1} v_1 + \frac{1 - \frac{m_1}{m_2}}{\frac{m_1}{m_2} + 1} v_2 \right) \\
    &= 0 \cdot v_1 + \frac{1}{1} v_2 \\
    &= v_2
\end{align}
$$

## Final Result

- $u_1 = \frac{m_1 - m_2}{m_1 + m_2} v_1 + \frac{2 m_2}{m_1 + m_2} v_2$
- $u_2 = \frac{2 m_1}{m_1 + m_2} v_1 + \frac{m_2 - m_1}{m_1 + m_2} v_2$
- For identical masses ($m_1 = m_2$): the particles perfectly exchange velocities ($u_1 = v_2$, $u_2 = v_1$).
- For a massive target ($m_2 \gg m_1$): the heavy mass continues unperturbed ($u_2 \approx v_2$), while the light mass bounces back with inverted relative speed ($u_1 \approx -v_1 + 2v_2$).

## Interpretation

The exact exchange of velocities for equal masses is characteristic of identical perfectly elastic particles (such as ideal billiard balls or Newton's cradle). In the case of extreme mass difference, the massive object acts essentially as a moving rigid wall; the light object rebounds elastically, preserving its speed relative to the heavy object, while the heavy object's momentum is barely affected.