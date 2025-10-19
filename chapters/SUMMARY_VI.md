
# Paper VI — Stability of the Quasi-Radial Modes (Hartle, Thorne & Chitre 1972)

**PDF:** [VI.pdf](sandbox:/mnt/data/VI.pdf)

## Goal
Develop **dynamical perturbation theory** for **quasi-radial oscillations** of a **slowly and rigidly rotating** relativistic star to $\mathcal{O}(\Omega^2)$. Compute the **rotation-induced shift** of oscillation frequencies without solving the full 2D problem.

## Framework
- Expand all quantities in amplitude $\epsilon$ (oscillation) and in $\Omega$ (rotation).  
- Seek normal modes with time dependence $\exp(i\omega t)$.  
- Derive a **functional (integral) expression** for the $\mathcal{O}(\Omega^2)$ correction to the squared frequency $\omega^2$, schematically:
```math
[\omega^2]^{(2)} = \frac{\int_0^R \Xi^{(2)}[\,\text{background},\,\text{radial eigenfunction},\,\text{rot. fields}\,]\,dr}{\int_0^R \mathcal{N}[\,\text{background},\,\text{radial eigenfunction}\,]\,dr},
```
where the numerator $\Xi^{(2)}$ depends on the **first-order frame-dragging** and **second-order** $\ell=0$ pieces.

## Physical Content
- **Centrifugal flattening** and frame dragging shift the frequencies of the radial modes; typically the **fundamental mode** is *stiffened* (frequency increases) modestly in the slow-rotation regime.  
- This complements the **static** turning-point analysis: here you get actual **mode frequencies** (and, in principle, damping by gravitational radiation for non-radial couplings).

## Assumptions & Caveats
- Assumes **non-degeneracy** of the underlying radial mode. Near **neutral stability** in isentropic stars, **degeneracy with convective modes** appears; then **non-degenerate** perturbation theory fails — see the IIIA correction for the static case and the cautionary discussion here.

## Output
- A **recipe** to evaluate $[\omega^2]^{(2)}$ given a non-rotating radial eigenfunction and the Paper I rotating background fields.  
- Sets the stage for **Paper VIII** (numerical evaluation for $n=3/2$).  
