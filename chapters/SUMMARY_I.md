
# Paper I — Slowly Rotating Relativistic Stars: Equations of Structure (Hartle 1967)

**PDF:** [I.pdf](sandbox:/mnt/data/I.pdf)

## Context & Goal
Derive a self-contained set of ordinary differential equations (ODEs) that determine the structure of a **rigidly, slowly rotating** relativistic star up to **$\mathcal{O}(\Omega^2)$**, starting from a static TOV background. This avoids the full 2D PDE problem by using a controlled perturbation expansion in the angular velocity $\Omega$.

## Assumptions
- **Barotropic EOS:** $P=P(E)$ (isentropic, one-parameter).  
- **Rigid rotation:** $\Omega=\mathrm{const}$ as seen at infinity.  
- **Stationary, axisymmetric, equatorially symmetric** configuration.  
- **Slow rotation:** small parameter $\Omega$ with
```math
\Omega^2 \ll \frac{M}{R^3}, \qquad v_{\rm eq}=\Omega R \ll c,
```
so all fractional changes are $\ll 1$.

## Background (non-rotating)
Metric (Schwarzschild-like):
```math
ds^2= -e^{2\Phi(r)}dt^2 + \left(1-\frac{2M(r)}{r}\right)^{-1}dr^2 + r^2(d\theta^2+\sin^2\theta\,d\phi^2).
```
TOV:
```math
\frac{dM}{dr}=4\pi r^2 E, \qquad
\frac{dP}{dr}=-\frac{(E+P)\left[M+4\pi r^3 P\right]}{r\left(r-2M\right)}, \qquad
\frac{d\Phi}{dr}=-\frac{1}{E+P}\frac{dP}{dr}.
```

## Perturbed metric and variables (to $\mathcal{O}(\Omega^2)$)
Use a Legendre expansion ($\ell=0,2$) with a frame-dragging term $g_{t\phi}$:
```math
\begin{aligned}
ds^2 = &-e^{2\Phi(r)}\Big[1+2h_0(r)+2h_2(r)P_2(\cos\theta)\Big]dt^2 \\
&+ \left(1-\frac{2M}{r}\right)^{-1}
\left[1+\frac{2m_0(r)+2m_2(r)P_2(\cos\theta)}{r-2M}\right]dr^2 \\
&+ r^2\Big[1+2k_0(r)+2k_2(r)P_2(\cos\theta)\Big]\{d\theta^2+\sin^2\theta[d\phi-\omega(r)dt]^2\}.
\end{aligned}
```
Fluid perturbations:
```math
P(r,\theta)=P_0(r)+(E_0+P_0)\big[p_0^\*(r)+p_2^\*(r)P_2(\cos\theta)\big], \quad \text{etc.}
```

## First order: frame dragging
Let $\bar\omega(r)=\Omega-\omega(r)$ and
```math
j(r)=e^{-\Phi}\sqrt{1-\frac{2M}{r}}.
```
The $t\phi$ field equation reduces to
```math
\frac{1}{r^4}\frac{d}{dr}\!\left(r^4 j \frac{d\omega}{dr}\right)+\frac{4}{r}\frac{d\omega}{dr}=0.
```
Outside:
```math
\omega(r)=\Omega-\frac{2J}{r^3},\qquad J=\frac{R^4}{6}\omega'(R),\qquad I=\frac{J}{\Omega}.
```

## Second order: $\ell=0$ (spherical) and $\ell=2$ (quadrupole) sectors
Spherical ($m_0,\,p_0^\*$) encode the **mass increment** and uniform pressure shift; quadrupolar ($h_2,k_2,p_2^\*$) encode the **oblateness** and **mass quadrupole** $Q$. Typical $\ell=0$ structure:
```math
\begin{aligned}
\frac{dm_0}{dr}&=4\pi r^2 \frac{dE}{dP}(E+P)\,p_0^\*(r)+\frac{1}{3}r^3\frac{d}{dr}\Big[r^2\bar\omega(r)^2\Big],\\
\frac{dp_0^\*}{dr}&=-\Phi'(r)\frac{dE/dP}{E+P}\,p_0^\*(r)-\frac{1}{3}\frac{r^3}{r-2M}\,\bar\omega(r)^2.
\end{aligned}
```
Mass correction:
```math
\delta M = m_0(R)+\frac{J^2}{R^3}.
```
Quadrupole sector matches to the external $\sim Q/r^3$ behavior to extract $Q$; Newtonian limit recovers **Clairaut’s equation** for ellipsoidal figures.

## Key Results
- A closed **ODE system** (TOV + frame dragging + $\ell=0,2$) to build rotating stars to $\mathcal{O}(\Omega^2)$.  
- **Moment of inertia** $I=J/\Omega$ via first-order integration of $\omega(r)$.  
- **Rotational mass increment** $\delta M$ and **quadrupole** $Q$ from second-order fields.  
- Clear **matching conditions** at $r=R$ fix $J$, $I$, $\delta M$, $Q$.

## Practical Use
1. Solve TOV $\to$ background $M(r),P(r),\Phi(r)$.  
2. Integrate frame dragging $\to$ $J,\,I$.  
3. Integrate $\ell=0,2$ $\to$ $\delta M,\,Q$ and shape.  
4. Check Newtonian limit; sanity-check signs ($Q<0$ oblate).

## Limitations
- Valid only while $\Omega^2 R^3/M\ll1$ and $v_{\rm eq}\ll c$.  
- Rigid rotation and barotropy; differential rotation handled later (Paper IV).

