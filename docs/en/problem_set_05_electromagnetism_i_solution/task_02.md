# Task 02 – Coulomb's Force

## Problem Statement

Two point charges are given:

$$
q_1 = 3 \ \mu\mathrm{C}, \quad q_2 = -5 \ \mu\mathrm{C}
$$

located at points:

$$
\vec{r}_1 = (0,0) \ \mathrm{m}, \quad \vec{r}_2 = (0.4, 0.3) \ \mathrm{m}
$$

1. Determine the force vector acting on $q_2$.
2. Calculate its magnitude.
3. Determine the potential energy of the system.
4. Calculate the work required to separate the charges to a distance of $2 \ \mathrm{m}$.

## Theory

The electrostatic force exerted by point charge $q_1$ on point charge $q_2$ is given by Coulomb's Law in vector form:

$$
\vec{F}_{12} = k \frac{q_1 q_2}{|\vec{r}_{12}|^2} \hat{r}_{12}
$$

where $k \approx 9 \times 10^9 \ \mathrm{N \cdot m^2 / C^2}$ is Coulomb's constant, $\vec{r}_{12} = \vec{r}_2 - \vec{r}_1$ is the relative position vector pointing from $q_1$ to $q_2$, and $\hat{r}_{12} = \frac{\vec{r}_{12}}{|\vec{r}_{12}|}$ is the unit vector in that direction.

The electric potential energy $U$ of a two-charge system separated by a distance $r$ is:

$$
U = k \frac{q_1 q_2}{r}
$$

The external work $W$ required to change the configuration of the system from an initial distance $r_i$ to a final distance $r_f$ is equal to the change in electric potential energy:

$$
W = \Delta U = U_f - U_i
$$

## Step-by-Step Solution

### 1. Force vector acting on $q_2$

First, determine the relative position vector $\vec{r}_{12}$ and the distance between the charges $r$:

$$
\begin{align}
\vec{r}_{12} &= \vec{r}_2 - \vec{r}_1 \\
             &= (0.4 - 0, 0.3 - 0) \ \mathrm{m} \\
             &= (0.4, 0.3) \ \mathrm{m}
\end{align}
$$

The scalar distance $r$ is the magnitude of this vector:

$$
\begin{align}
r &= \sqrt{0.4^2 + 0.3^2} \\
  &= \sqrt{0.16 + 0.09} \\
  &= \sqrt{0.25} \\
  &= 0.5 \ \mathrm{m}
\end{align}
$$

The unit vector $\hat{r}_{12}$ is:

$$
\begin{align}
\hat{r}_{12} &= \frac{(0.4, 0.3)}{0.5} \\
             &= (0.8, 0.6)
\end{align}
$$

Now, evaluate the force vector $\vec{F}_2$:

$$
\begin{align}
\vec{F}_2 &= \left( 9 \times 10^9 \right) \frac{(3 \times 10^{-6})(-5 \times 10^{-6})}{(0.5)^2} (0.8, 0.6) \\
          &= \frac{-135 \times 10^{-3}}{0.25} (0.8, 0.6) \\
          &= -0.54 (0.8, 0.6) \ \mathrm{N} \\
          &= (-0.432, -0.324) \ \mathrm{N}
\end{align}
$$

### 2. Magnitude of the force

The magnitude can be calculated directly from the scalar form of Coulomb's Law, or by taking the magnitude of the force vector:

$$
\begin{align}
|\vec{F}_2| &= \sqrt{(-0.432)^2 + (-0.324)^2} \\
            &= \sqrt{0.186624 + 0.104976} \\
            &= \sqrt{0.2916} \\
            &= 0.54 \ \mathrm{N}
\end{align}
$$

Alternatively, using the previously calculated scalar part:

$$
\begin{align}
|\vec{F}_2| &= \left| -0.54 \right| \\
            &= 0.54 \ \mathrm{N}
\end{align}
$$

### 3. Potential energy of the system

Substituting the known values into the potential energy equation with $r_i = 0.5 \ \mathrm{m}$:

$$
\begin{align}
U_i &= \left( 9 \times 10^9 \right) \frac{(3 \times 10^{-6})(-5 \times 10^{-6})}{0.5} \\
    &= \frac{-135 \times 10^{-3}}{0.5} \\
    &= -0.27 \ \mathrm{J}
\end{align}
$$

### 4. Work required to separate the charges

First, calculate the final potential energy $U_f$ at the new distance $r_f = 2 \ \mathrm{m}$:

$$
\begin{align}
U_f &= \left( 9 \times 10^9 \right) \frac{(3 \times 10^{-6})(-5 \times 10^{-6})}{2} \\
    &= \frac{-135 \times 10^{-3}}{2} \\
    &= -0.0675 \ \mathrm{J}
\end{align}
$$

The required external work is the difference between final and initial states:

$$
\begin{align}
W &= U_f - U_i \\
  &= -0.0675 \ \mathrm{J} - (-0.27 \ \mathrm{J}) \\
  &= -0.0675 \ \mathrm{J} + 0.27 \ \mathrm{J} \\
  &= 0.2025 \ \mathrm{J}
\end{align}
$$

## Final Result

1. $\vec{F}_2 = (-0.432, -0.324) \ \mathrm{N}$
2. $|\vec{F}_2| = 0.54 \ \mathrm{N}$
3. $U = -0.27 \ \mathrm{J}$
4. $W = 0.2025 \ \mathrm{J}$

## Interpretation

The negative sign in the potential energy indicates an attractive system; the charges are bound to each other. Because they have opposite signs, the force vector points in the opposite direction of the displacement vector, confirming the attractive nature of the force. Separating the charges to a larger distance requires an external agent to overcome this attraction, which is mathematically represented by the positive work value ($0.2025 \ \mathrm{J}$) added to the system.