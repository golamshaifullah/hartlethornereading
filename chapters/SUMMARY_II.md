
# Paper II — Models for Neutron Stars and Supermassive Stars (Hartle & Thorne 1968)

**PDF:** [II.pdf](sandbox:/mnt/data/II.pdf)

## Aim
Apply the Paper I equations to **realistic EOS** (white dwarf / neutron star matter) and to **polytropes** (notably $n=3$) to compute rotating stellar sequences: $M$, $R$, $I$, $Q$, and surface flattening vs. central density.

## Setup
- **EOS choices:** cold degenerate matter for WDs/NSs (tabulated) and **polytropic $n=3$** for supermassive stars.  
- For each central density $E_c$, build the **non-rotating** TOV model, then add rotation with a fixed, normalized $\Omega$ (often scaled by a convenient upper bound).

## Equations used (from Paper I)
- **TOV** for background.  
- **Frame dragging** (first order) to obtain $J$ and $I$.  
- **Second-order** $\ell=0$ (spherical) and $\ell=2$ (quadrupole) systems to get $\delta M$, $Q$, and surface flattening.

## Representative Relations
Moment of inertia:
```math
I=\frac{J}{\Omega},\qquad \omega(r)=\Omega-\frac{2J}{r^3}\ \ (r\ge R).
```
Mass increment:
```math
\delta M = m_0(R)+\frac{J^2}{R^3}.
```

## Results (Qualitative Highlights)
- **Neutron stars (realistic EOS):** rotation **increases $M$ and $R$** for fixed $E_c$; $I$ rises with compactness; $Q<0$ indicates oblate deformation.  
- **White dwarfs:** similar qualitative behavior at much larger radii, smaller compactness.  
- **$n=3$ polytropes (supermassive):** show how even mild rotation can affect equilibrium before nuclear burning; quantify the modest stabilizing trend against immediate collapse.

## Tables/Plots
The paper reports **tabulated sequences** and **graphs** (e.g., $M(R)$, $I(M)$, flattening vs. $E_c$), which are useful benchmarks for codes implementing Paper I.

## How to Use
- Validate your integrator by reproducing one of the published sequences (e.g., a polytrope).  
- Use the **exterior matching** to check $I$ and $Q$.  
- Compare **non-rotating vs rotating** curves to quantify rotational effects for your EOS.

## Limitations
- Slow-rotation domain only; does not capture mass-shedding onset precisely.  
- Rigid rotation and barotropic EOS remain in force.
