# Task 02 – Inclined plane with friction

## Problem Statement

A body of mass $m$ slides down an inclined plane with an angle $\alpha$. The coefficient of kinetic friction is $\mu$.

Determine:
1. All forces acting on the body.
2. The acceleration magnitude $a$ and vector direction.
3. The time of descent $t$ from a vertical height $h$.
4. The final velocity magnitude $v$.
5. The consistency of the result with the mechanical energy balance.

## Theory

The standard coordinate system for an inclined plane aligns the $x$-axis parallel to the surface (pointing downwards) and the $y$-axis perpendicular to the surface (pointing upwards). 

The normal force balances the perpendicular component of gravity. The kinetic friction force opposes the direction of motion and is proportional to the normal force:

$$
f_k = \mu N
$$

The distance traveled along the incline $d$ relates to the vertical height $h$ via trigonometry:

$$
\sin\alpha = \frac{h}{d} \implies d = \frac{h}{\sin\alpha}
$$

The work done by non-conservative forces (friction) equals the change in total mechanical energy.

## Step-by-Step Solution

### 1. Forces acting on the body

- **Gravity ($\vec F_g$):** Magnitude $mg$, pointing strictly downward.
- **Normal force ($\vec N$):** Magnitude $N$, pointing perpendicular to the plane, outward.
- **Kinetic friction ($\vec f_k$):** Magnitude $\mu N$, pointing up the incline (opposing motion).

Decomposing gravity into components parallel and perpendicular to the incline:

$$
F_{gx} = mg \sin\alpha
$$

$$
F_{gy} = -mg \cos\alpha
$$

### 2. Acceleration

Apply Newton's second law in the perpendicular ($y$) direction, where acceleration is zero:

$$
\sum F_y = N - mg \cos\alpha = 0
$$

$$
N = mg \cos\alpha
$$

Therefore, the magnitude of the friction force is:

$$
f_k = \mu mg \cos\alpha
$$

Apply Newton's second law in the parallel ($x$) direction:

$$
\sum F_x = mg \sin\alpha - f_k = ma
$$

$$
mg \sin\alpha - \mu mg \cos\alpha = ma
$$

Divide by $m$:

$$
a = g(\sin\alpha - \mu \cos\alpha)
$$

The vector $\vec a$ points down the incline.

### 3. Time of descent

The body starts from rest ($v_0 = 0$) and travels a distance $d = \frac{h}{\sin\alpha}$ under constant acceleration.

$$
d = \frac{1}{2} a t^2
$$

Solve for $t$:

$$
\begin{align}
t &= \sqrt{\frac{2d}{a}} \\
  &= \sqrt{\frac{2 \left( \frac{h}{\sin\alpha} \right)}{g(\sin\alpha - \mu \cos\alpha)}} \\
  &= \sqrt{\frac{2h}{g \sin\alpha (\sin\alpha - \mu \cos\alpha)}}
\end{align}
$$

### 4. Final velocity

Using the kinematic relation $v^2 = v_0^2 + 2ad$:

$$
\begin{align}
v &= \sqrt{2ad} \\
  &= \sqrt{2 \cdot g(\sin\alpha - \mu \cos\alpha) \cdot \frac{h}{\sin\alpha}} \\
  &= \sqrt{\frac{2gh(\sin\alpha - \mu \cos\alpha)}{\sin\alpha}}
\end{align}
$$

### 5. Energy balance

The initial mechanical energy is purely potential:

$$
E_i = mgh
$$

The final mechanical energy is purely kinetic:

$$
\begin{align}
E_f &= \frac{1}{2} m v^2 \\
    &= \frac{1}{2} m \left( \frac{2gh(\sin\alpha - \mu \cos\alpha)}{\sin\alpha} \right) \\
    &= mgh - mgh \mu \frac{\cos\alpha}{\sin\alpha} \\
    &= mgh - \mu mg h \cot\alpha
\end{align}
$$

The work done by friction is:

$$
\begin{align}
W_f &= -f_k d \\
    &= -(\mu mg \cos\alpha) \left( \frac{h}{\sin\alpha} \right) \\
    &= -\mu mg h \cot\alpha
\end{align}
$$

The energy balance equation states $E_f - E_i = W_f$:

$$
(mgh - \mu mg h \cot\alpha) - mgh = -\mu mg h \cot\alpha
$$

This equality holds perfectly.

## Final Result

- $a = g(\sin\alpha - \mu \cos\alpha)$
- $t = \sqrt{\frac{2h}{g \sin\alpha (\sin\alpha - \mu \cos\alpha)}}$
- $v = \sqrt{\frac{2gh(\sin\alpha - \mu \cos\alpha)}{\sin\alpha}}$
- The energy balance is strictly satisfied.

## Interpretation

The acceleration depends on both the steepness of the incline and the roughness of the surface. If $\mu \ge \tan\alpha$, the acceleration becomes zero or negative, meaning the body will not slide from rest. The dissipated energy manifests mechanically as the work done by friction, lowering the final kinetic energy compared to a frictionless drop.