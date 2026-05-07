# Task 05 – Capacitor: energy and force

## Problem Statement

We have a parallel plate capacitor:
* $S = 0.02 \ \mathrm{m^2}$
* $d = 5 \ \mathrm{mm} = 5 \times 10^{-3} \ \mathrm{m}$
* $U = 500 \ \mathrm{V}$

Answer the following questions:
1. Calculate the capacitance.
2. Calculate the energy stored in the capacitor.
3. Calculate the electric field intensity between the plates.
4. Calculate the field energy density.
5. Calculate the force of attraction between the plates.

## Theory

The capacitance $C$ of an ideal parallel plate capacitor with a vacuum (or air, approximately) between its plates is given by:

$$
C = \varepsilon_0 \frac{S}{d}
$$

where $\varepsilon_0 \approx 8.854 \times 10^{-12} \ \mathrm{F/m}$ is the vacuum permittivity, $S$ is the surface area of one plate, and $d$ is the separation distance.

The total potential energy $W$ stored in a capacitor charged to a voltage $U$ is:

$$
W = \frac{1}{2} C U^2
$$

In a parallel plate capacitor, the electric field $\vec{E}$ between the plates is uniform (ignoring edge effects). Its magnitude $E$ is related to the potential difference $U$ by:

$$
E = \frac{U}{d}
$$

The energy density $u$, which represents the energy stored per unit volume of the electric field, is calculated as:

$$
u = \frac{1}{2} \varepsilon_0 E^2
$$

The electrostatic force of attraction $F$ between the two plates arises because the charges on the plates are opposite. It can be derived from the principle of virtual work ($F = \frac{dW}{dd}$ at constant charge) or calculated using the energy density multiplied by the plate area:

$$
F = u S = \frac{1}{2} \varepsilon_0 E^2 S
$$

## Step-by-Step Solution

### 1. Capacitance

Substituting the given geometric parameters and the vacuum permittivity:

$$
\begin{align}
C &= (8.854 \times 10^{-12}) \frac{0.02}{5 \times 10^{-3}} \\
  &= (8.854 \times 10^{-12}) (4) \\
  &= 35.416 \times 10^{-12} \ \mathrm{F}
\end{align}
$$

### 2. Energy stored in the capacitor

Using the calculated capacitance and the given voltage:

$$
\begin{align}
W &= \frac{1}{2} (35.416 \times 10^{-12}) (500)^2 \\
  &= (17.708 \times 10^{-12}) (250000) \\
  &= 4.427 \times 10^{-6} \ \mathrm{J}
\end{align}
$$

### 3. Electric field intensity

The uniform electric field magnitude is:

$$
\begin{align}
E &= \frac{500}{5 \times 10^{-3}} \\
  &= 100000 \ \mathrm{V/m} \\
  &= 10^5 \ \mathrm{V/m}
\end{align}
$$

### 4. Field energy density

Substituting the electric field intensity into the energy density formula:

$$
\begin{align}
u &= \frac{1}{2} (8.854 \times 10^{-12}) (10^5)^2 \\
  &= (4.427 \times 10^{-12}) (10^{10}) \\
  &= 4.427 \times 10^{-2} \ \mathrm{J/m^3}
\end{align}
$$

Alternatively, this can be verified by dividing the total stored energy by the volume between the plates ($V = S \cdot d$):

$$
\begin{align}
u &= \frac{W}{S d} \\
  &= \frac{4.427 \times 10^{-6}}{(0.02)(0.005)} \\
  &= \frac{4.427 \times 10^{-6}}{10^{-4}} \\
  &= 4.427 \times 10^{-2} \ \mathrm{J/m^3}
\end{align}
$$

### 5. Force of attraction

The attractive force is the product of the energy density and the plate area:

$$
\begin{align}
F &= (4.427 \times 10^{-2}) (0.02) \\
  &= 8.854 \times 10^{-4} \ \mathrm{N}
\end{align}
$$

## Final Result

1. $C \approx 35.4 \ \mathrm{pF}$
2. $W \approx 4.43 \ \mu\mathrm{J}$
3. $E = 100 \ \mathrm{kV/m}$
4. $u \approx 0.0443 \ \mathrm{J/m^3}$
5. $F \approx 0.885 \ \mathrm{mN}$

## Interpretation

The parallel plate capacitor geometry stores electrical energy entirely within the uniform electric field established between the plates. The energy density $u$ demonstrates that energy storage is directly proportional to the square of the electric field intensity. The physical consequence of this stored potential is a mechanical force of attraction between the oppositely charged plates. Although the voltage ($500 \ \mathrm{V}$) and field ($100 \ \mathrm{kV/m}$) are relatively high, the overall capacitance is very small (in the picofarad range) due to the macroscopic plate separation and lack of a dielectric medium, resulting in a relatively small stored energy and weak mechanical force.