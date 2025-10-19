
# Paper IV — Rotational Energy and Moment of Inertia for Stars in Differential Rotation (Hartle 1970)

**PDF:** [IV.pdf](sandbox:/mnt/data/IV.pdf)

## Purpose
Generalize the slow-rotation energetics to **differential rotation** and derive clean relations for the **rotational contribution to the mass-energy** and the **moment of inertia** to $\mathcal{O}(\Omega^2)$.

## Main Relations
For a prescribed slow rotation law $\Omega(\text{position})$, the **rotational energy** is
```math
M_{\rm rot} = \frac{1}{2}\int \Omega\, dJ,
```
which reduces, for **uniform rotation**, to
```math
M_{\rm rot} = \frac{1}{2} I \Omega^2 + \mathcal{O}(\Omega^4).
```
Here, $I \equiv J/\Omega$ is the relativistic **moment of inertia**. These hold **without** solving the full second-order structural system; they follow from a variational formulation of equilibrium.

## Content Highlights
- **Variational derivation**: uses the stationary action/energy principles for slowly rotating equilibria to connect $M$, $J$, and $\Omega$.  
- **Upper/lower bounds** on $M_{\rm rot}$, positivity proofs for general differential rotation laws in the slow limit.  
- Clarifies **how to compute $I$** and $M_{\rm rot}$ from **first-order** frame-dragging information (Paper I) plus the rotation law.

## Why It’s Useful
When only global energetic effects are needed (e.g., total rotational energy at fixed baryon number/entropy profile), you can **avoid** the full $\ell=0,2$ integrations and use these compact expressions.

## Caveats
- Still limited to the **slow-rotation** regime.  
- The **rotation law** must be specified and consistent with hydrostatic equilibrium to $\mathcal{O}(\Omega^2)$ (barotropic fluid).  
