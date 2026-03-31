# Task 05 – Superposition of waves, beats, and group velocity

## Problem Statement

Two harmonic waves are given:

$$
y_1(x,t) = A\sin(kx-\omega t)
$$

$$
y_2(x,t) = A\sin(kx-(\omega+\Delta\omega)t)
$$

Determine:
1. The resultant wave $y = y_1 + y_2$ in product form (carrier × envelope).
2. The beat frequency and beat period at $x=0$.
3. The physical interpretation of the envelope and carrier wave.
4. The framework to generate the waves and beats using HTML/JS/Python.

## Theory

The principle of superposition dictates that when two or more waves traverse the same space, the net displacement is the algebraic sum of the individual displacements.

When two waves of equal amplitude but slightly different frequencies interfere, they produce a phenomenon called beats. The mathematical transformation relies on the trigonometric sum-to-product identity:

$$
\sin \alpha + \sin \beta = 2 \sin\left(\frac{\alpha + \beta}{2}\right) \cos\left(\frac{\alpha - \beta}{2}\right)
$$

## Step-by-Step Solution

### 1. Resultant wave in product form

Define the arguments of the sine functions:

$$
\alpha = kx - \omega t
$$

$$
\beta = kx - (\omega + \Delta\omega)t
$$

Compute the sum and difference of the arguments:

$$
\begin{align}
\alpha + \beta &= 2kx - (2\omega + \Delta\omega)t \\
\alpha - \beta &= \Delta\omega t
\end{align}
$$

Apply the trigonometric identity to $y(x,t) = y_1(x,t) + y_2(x,t)$:

$$
\begin{align}
y(x,t) &= A \left[ \sin(\alpha) + \sin(\beta) \right] \\
       &= 2A \sin\left(\frac{2kx - (2\omega + \Delta\omega)t}{2}\right) \cos\left(\frac{\Delta\omega t}{2}\right) \\
       &= \left[ 2A \cos\left(\frac{\Delta\omega}{2} t\right) \right] \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)
\end{align}
$$

The result is the product of a slowly varying envelope function and a rapidly oscillating carrier wave.

### 2. Beat frequency and period at $x=0$

At $x=0$, the wave function simplifies to:

$$
y(0,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2} t\right) \right] \sin\left(-\left(\omega + \frac{\Delta\omega}{2}\right)t\right)
$$

The amplitude of the combined wave is modulated by the absolute value of the envelope term: $\left| 2A \cos\left(\frac{\Delta\omega}{2} t\right) \right|$.

Since the cosine function reaches a maximum magnitude (both positive and negative peaks) twice per full cycle, the frequency of the amplitude maxima (the beat frequency $f_{beat}$) is twice the frequency of the envelope function itself.

The angular frequency of the envelope is $\omega_{env} = \frac{\Delta\omega}{2}$. The angular beat frequency is:

$$
\omega_{beat} = 2 \omega_{env} = \Delta\omega
$$

The linear beat frequency is:

$$
f_{beat} = \frac{\Delta\omega}{2\pi} = \Delta f
$$

The beat period $T_{beat}$ is the reciprocal of the beat frequency:

$$
T_{beat} = \frac{1}{f_{beat}} = \frac{2\pi}{\Delta\omega}
$$

### 3. Physical Interpretation

- **Carrier Wave:** Represented by the high-frequency sine term, $\sin\left(kx - (\omega + \Delta\omega/2)t\right)$. It describes the rapid, localized oscillation of the medium particles at an average angular frequency of $\omega + \Delta\omega/2$. The phase velocity defines the speed of these individual ripples.
- **Envelope:** Represented by the slowly varying cosine term, $2A \cos(\frac{\Delta\omega}{2} t)$. It dictates the macroscopic amplitude modulation of the wave packet. In dispersive media where waves of different frequencies travel at different speeds, the envelope propagates at the group velocity, which defines the speed at which the overall energy and information of the wave packet travel.

### 4. Computational Framework

To visualize this dynamically:
1. Compute arrays for $y_1$ and $y_2$ over a defined time array $t$ at a fixed $x=0$.
2. Compute the superposition $y = y_1 + y_2$.
3. Compute the envelope boundaries $+2A \cos(\Delta\omega t / 2)$ and $-2A \cos(\Delta\omega t / 2)$.
4. Plot $y$ as a dense, rapidly oscillating line and overlay the envelope boundaries as dashed, slowly varying lines encompassing the carrier wave.

## Final Result

- $y(x,t) = \left[ 2A \cos\left(\frac{\Delta\omega}{2} t\right) \right] \sin\left(kx - \left(\omega + \frac{\Delta\omega}{2}\right)t\right)$
- $f_{beat} = \frac{\Delta\omega}{2\pi}$
- $T_{beat} = \frac{2\pi}{\Delta\omega}$

## Interpretation

Beats are a direct manifestation of wave interference in the time domain. When two frequencies are very close, they periodically drift in and out of phase, creating a slow modulation in amplitude that human ears perceive as a pulsing volume or "wah-wah" effect, heavily utilized in tuning musical instruments.