- [ ] Cleanup math formatting for GFM

# Slowly Rotating Relativistic Stars — Starter Pack

This repository contains:
- **A concise, self-contained introduction** to the Hartle–Thorne slow-rotation formalism (Papers I–VIII).
- **A minimal Jupyter notebook** that integrates the Tolman–Oppenheimer–Volkoff (TOV) equations and the first-order frame-dragging equation for a toy gamma-law EOS, so you can reproduce the core quantities $$M$$, $$R$$, and $$I=J/\Omega$$ for a slowly rotating star.

Jump to the notebook: **[tov_frame_dragging.ipynb](notebooks/tov_frame_dragging.ipynb)**

---

## 1) Static equilibrium (TOV)

```math
ds^2 = -e^{2\Phi(r)}dt^2 + \left(1-\frac{2M(r)}{r}\right)^{-1}dr^2 + r^2(d\theta^2+\sin^2\theta\,d\phi^2).
```

Perfect fluid: $$T_{\mu\nu}=(E+P)u_\mu u_\nu + P g_{\mu\nu}$$.

```math
\frac{dM}{dr} = 4\pi r^2 E, \qquad
\frac{dP}{dr} = -\frac{(E+P)\left[M+4\pi r^3 P\right]}{r\left(r-2M\right)}.
```

Auxiliary:
```math
\frac{d\Phi}{dr} = -\frac{1}{E+P}\frac{dP}{dr}.
```

Surface where $$P(R)=0$$; then $$M(R)=M$$.

---

## 2) EOS and the slow-rotation setup

We assume a **barotropic** EOS $$P=P(E)$$. In the demo notebook we use a simple **gamma-law EOS** for pedagogy:
```math
P = K\,\rho^{\gamma},\qquad E = \rho + \frac{P}{\gamma-1}.
```

In the Hartle–Thorne formalism (Paper I), slow rigid rotation at angular velocity $$\Omega$$ introduces:
- First order (in $$\Omega$$): frame-dragging $$g_{t\phi}$$, with local inertial frames rotating at $$\omega(r)$$.
- Second order (in $$\Omega^2$$): spherical corrections ($$\ell=0$$) to mass/pressure and quadrupolar ($$\ell=2$$) shape $$\Rightarrow$$ oblate star and quadrupole $$Q$$.

---

## 3) Frame dragging (first order)

Define the fluid’s angular velocity relative to local frames:
```math
\bar{\omega}(r) = \Omega - \omega(r).
```
The standard first-order ODE for $$\bar{\omega}$$ is
```math
\frac{d}{dr}\Bigl(r^4 j(r) \frac{d\bar{\omega}}{dr}\Bigr) + 4 r^3 \frac{dj}{dr} \, \bar{\omega} = 0,
\quad
j(r) = e^{-\Phi(r)}\sqrt{1-\frac{2M(r)}{r}}.
```
Boundary conditions: regular at the center ($$d\bar{\omega}/dr\rvert_0=0$$). Outside the star,
```math
\bar{\omega}(r) = \frac{2J}{r^3},
```
so the **moment of inertia** is $$I=J/\Omega$$. In the notebook we set $$\Omega=1$$ (pure scaling), integrate $$\bar{\omega}$$, and read off $$J$$ from the surface behavior, so **$$I=J$$** in those units.

---

## 4) What you get from the notebook

Given $$K,\gamma, P_c$$, the notebook:
- Integrates **TOV** to obtain $$M(r), P(r), E(r), \Phi(r)$$ and the surface $$R$$.
- Integrates **frame dragging** for $$\bar{\omega}(r)$$ and reports **$$I$$** via the asymptotic matching.
- Plots $$M(r), P(r), \bar{\omega}(r)$$.

You can sweep parameters to build sequences $$M(P_c), I(M)$$, etc.

---

## 5) Minimal references (clickable)

These are the specific PDFs you provided (organized as Papers I–VIII). Open them directly from here:

- **Paper I** — Hartle (1967), *Slowly Rotating Relativistic Stars I. Equations of Structure* — [SUMMARY\_I.md](chapters/SUMMARY\_I.md)
- **Paper II** — Hartle & Thorne (1968), *Models for Neutron Stars and Supermassive Stars* — [SUMMARY\_II.md](chapters/SUMMARY\_II.md)
- **Paper III** — Hartle & Thorne (1969), *Static Criterion for Stability* — [SUMMARY\_III.md](chapters/SUMMARY\_III.md)
- **Paper IIIA** — Hartle (1975), *The Static Stability Criterion Recovered* — [SUMMARY\_IIIA.md](chapters/SUMMARY\_IIIA.md)
- **Paper IV** — Hartle (1970), *Rotational Energy and Moment of Inertia for Stars in Differential Rotation* — [SUMMARY\_IV.md](chapters/SUMMARY\_IV.md)
- **Paper V** — Hartle & Munn (1975), *Static Stability Analysis of n=3/2 Polytropes* — [SUMMARY\_V.md](chapters/SUMMARY\_V.md)
- **Paper VI** — Hartle, Thorne & Chitre (1972), *Stability of the Quasi-Radial Modes* — [SUMMARY\_VI.md](chapters/SUMMARY\_VI.md)
- **Paper VIII** — Hartle & Friedman (1975), *Frequencies of the Quasi-Radial Modes of an n=3/2 Polytrope* — [SUMMARY\_VIII.md](chapters/SUMMARY\_VIII.md)

---

## 6) Notes on validity

This is the $$\mathcal{O}(\Omega^2)$$ slow-rotation regime. Don’t use it near mass-shedding or when $$\Omega^2 R^3/M$$ stops being $$\ll 1$$. For realistic EOS and precise quadrupoles $$Q$$, move beyond the toy gamma-law EOS and implement the $$\ell=0,2$$ second-order systems from Paper I.

---

**Open the notebook:** [tov_frame_dragging.ipynb](notebooks/tov_frame_dragging.ipynb)
