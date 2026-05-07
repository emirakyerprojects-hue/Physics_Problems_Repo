# Task 10 – Field flux (verification of Gauss's law)

## Problem Statement

1. Define the electric field flux.
2. Consider a sphere around a point charge.
3. Implement a discrete approximation of the flux.
4. Investigate the dependence on the number of grid points.
5. Compare with the analytical result.

## Theory

Gauss's Law states that the net electric flux $\Phi_E$ passing through any closed surface is proportional to the total electric charge $q_{\text{enc}}$ enclosed by that surface:

$$
\Phi_E = \oint_S \vec{E} \cdot d\vec{A} = \frac{q_{\text{enc}}}{\varepsilon_0}
$$

where $\vec{E}$ is the electric field vector, $d\vec{A}$ is the outward-pointing differential area vector, and $\varepsilon_0$ is the vacuum permittivity.

## Step-by-Step Solution

### 1. Definition of electric field flux

Electric flux is a scalar quantity representing the measure of the electric field penetrating a specific surface area. Mathematically, it is the surface integral of the normal component of the electric field over that surface. 

### 2. Sphere around a point charge

Consider a point charge $q$ located at the origin. We construct a fictitious spherical surface (Gaussian sphere) of radius $R$ centered on the charge. 

The electric field of a point charge at any point on the sphere is purely radial:

$$
\vec{E} = \frac{1}{4\pi\varepsilon_0} \frac{q}{R^2} \hat{r}
$$

The differential area vector for the sphere is also purely radial:

$$
d\vec{A} = \hat{r} \, dA = \hat{r} \, R^2 \sin\theta \, d\theta \, d\phi
$$

### 3. Discrete approximation of the flux

To approximate the integral numerically, the spherical surface is tessellated into a finite number $N$ of small discrete area patches $\Delta A_i$. Each patch has a normal vector $\hat{n}_i$.

The total flux is approximated by the Riemann sum:

$$
\Phi_E \approx \sum_{i=1}^{N} \vec{E}(\vec{r}_i) \cdot (\hat{n}_i \Delta A_i)
$$

Assuming the patches are evenly distributed such that $\Delta A_i \approx \frac{4\pi R^2}{N}$, and the normal vector is aligned with the radial position vector $\vec{r}_i$, the discrete formula is implemented computationally by iterating over all $N$ grid points, calculating the field vector at each point, projecting it onto the normal, and multiplying by the patch area.

### 4. Dependence on the number of grid points

The accuracy of the discrete approximation strongly depends on $N$, the number of grid points. 
* For a low value of $N$, the planar patches $\Delta A_i$ poorly approximate the curvature of the sphere, and the assumption that $\vec{E}$ is constant across the patch is violated, leading to significant numerical error.
* As $N \to \infty$, the discrete patches infinitesimally shrink ($\Delta A \to dA$), and the numerical sum converges asymptotically to the exact integral. The truncation error typically scales proportionally to $1/N$ or $1/N^2$ depending on the specific tessellation algorithm (e.g., Fibonacci lattice vs. latitude/longitude grid).

### 5. Comparison with the analytical result

Analytically, evaluating the flux integral for the Gaussian sphere:

$$
\begin{align}
\Phi_E &= \oint_S \left( \frac{1}{4\pi\varepsilon_0} \frac{q}{R^2} \hat{r} \right) \cdot (\hat{r} \, dA) \\
       &= \frac{q}{4\pi\varepsilon_0 R^2} \oint_S (\hat{r} \cdot \hat{r}) \, dA \\
       &= \frac{q}{4\pi\varepsilon_0 R^2} \oint_S dA
\end{align}
$$

Since the integral of $dA$ over the sphere is simply the total surface area $A = 4\pi R^2$:

$$
\begin{align}
\Phi_E &= \frac{q}{4\pi\varepsilon_0 R^2} (4\pi R^2) \\
       &= \frac{q}{\varepsilon_0}
\end{align}
$$

## Final Result

1. Flux definition: $\Phi_E = \int \vec{E} \cdot d\vec{A}$.
2. Spherical symmetry yields $\vec{E} \parallel d\vec{A}$.
3. Discrete sum algorithm: $\Phi_E \approx \sum \vec{E}_i \cdot \Delta \vec{A}_i$.
4. The numerical sum converges to the theoretical value as $N$ increases.
5. The analytical integration explicitly proves Gauss's law ($\Phi_E = q/\varepsilon_0$), entirely independent of the sphere's radius $R$.

## Interpretation

Gauss's law reveals a profound topological property of the inverse-square force law: the total number of field lines piercing an enclosing surface depends strictly on the charge contained inside, regardless of the size or shape of that surface. While the numerical approximation relies on summing field values over thousands of points, the analytical proof elegantly demonstrates that the $R^2$ scaling of the surface area perfectly cancels the $1/R^2$ decay of the field magnitude, conserving flux perfectly.