# Introduction and Framework for Slowly Rotating Relativistic Stars

Real stars rotate. If you ignore that, you get the wrong answers for radii, masses at stability limits, and pulsation frequencies. The good news: when rotation is **slow** relative to the mass-shedding limit, you can treat it as a perturbation of a spherical Tolman–Oppenheimer–Volkoff (TOV) star and push general relativity (GR) through to **$\mathcal{O}(\Omega^2)$** accuracy. That is the Hartle–Thorne slow-rotation program developed across Papers I–VIII you uploaded. What follows is the minimum mathematical framework to work through those papers—no fluff, just what you’ll use. 

---

## 1) Static equilibrium in GR (the base model)

Assume a static, spherically symmetric perfect fluid with the Schwarzschild-like metric
```math
ds^2
= -e^{2\Phi(r)}dt^2

* \left(1-\frac{2M(r)}{r}\right)^{-1}dr^2
* r^2(d\theta^2+\sin^2\theta,d\phi^2).
  $$
```
Stress–energy: $T_{\mu\nu}=(E+P)u_\mu u_\nu + P g_{\mu\nu}$, with total energy density $E$ and pressure $P$.

Mass continuity and hydrostatic balance (TOV):
$$
\frac{dM}{dr}=4\pi r^2 E,\qquad
\frac{dP}{dr}=-\frac{(E+P)\left[M+4\pi r^3 P\right]}{r\bigl(r-2M\bigr)}.
\tag{TOV}
$$

The redshift potential $\Phi$ obeys
$$
\frac{d\Phi}{dr}=-\frac{1}{E+P}\frac{dP}{dr},
$$
and $P(R)=0$ identifies the stellar surface $r=R$ with total mass $M(R)=M$. This is the non-rotating background solved in every subsequent paper. (Parameter choices and scaling tricks for specific EOS appear throughout Papers II and IV.)  

---

## 2) One-parameter equations of state (EOS)

All papers assume a barotropic EOS $P=P(E)$ (isentropic). You’ll use:

* **Cold degenerate matter**: realistic tabulations for white dwarfs / neutron stars (Paper II).
* **Polytropes**: $P=K\rho^{1+1/n}$ (Tooper relativistic polytropes). $n=3$ captures radiation-pressure dominated supermassive stars; $n=3/2$ ($\gamma=5/3$) is a workhorse toy model used in Papers V and VIII to test stability and mode formulas.   

*Why barotropic?* It aligns pressure and density isosurfaces, avoids baroclinic meridional flows at leading order, and keeps the slow-rotation scheme tractable. Hartle is explicit about this simplification from the outset. 

---

## 3) Slow rotation as a perturbation

Assume **rigid rotation** with constant angular velocity $\Omega$ (as seen at infinity), **stationarity**, **axisymmetry**, and **equatorial reflection symmetry**. Expand the metric and fluid variables in $\Omega$. Scalars (like $P,E$) shift first at $\mathcal{O}(\Omega^2)$ by symmetry; the only $\mathcal{O}(\Omega)$ effect is the **frame-dragging** $g_{t\phi}$ term. 

A convenient form of the interior metric to $\mathcal{O}(\Omega^2)$ is
$$
\begin{aligned}
ds^2 =&;

* e^{2\Phi(r)}\Bigl[1 + 2h_0(r) + 2h_2(r)P_2(\cos\theta)\Bigr],dt^2 \
  &+ \left(1-\frac{2M(r)}{r}\right)^{-1}
  \left[1 + \frac{2m_0(r)+2m_2(r)P_2(\cos\theta)}{r-2M(r)}\right]dr^2 \
  &+ r^2\Bigl[1 + 2k_0(r) + 2k_2(r)P_2(\cos\theta)\Bigr]
  \Bigl{d\theta^2 + \sin^2\theta,[d\phi-\omega(r)dt]^2\Bigr}

- \mathcal{O}(\Omega^3).
  \end{aligned}
  $$

Here:

* $\omega(r)$ is the **dragging of inertial frames** (first order in $\Omega$).
* $h_0,m_0,k_0$ (spherical, $\ell=0$) and $h_2,m_2,k_2$ (quadrupole, $\ell=2$) are all $\mathcal{O}(\Omega^2)$.
* Fluid perturbations are decomposed as $P(r,\theta)=P_0(r)+(E_0+P_0)\bigl[p_0^*(r)+p_2^*(r)P_2(\cos\theta)\bigr]$, and similarly for $E$.

This is the working ansatz of Paper I. You’ll derive and integrate ODEs for the unknown functions. 

---

## 4) First-order structure: frame dragging and $I=J/\Omega$

Define the fluid’s angular velocity **relative to local inertial frames**
$$
\bar{\omega}(r)\equiv \Omega-\omega(r).
$$
The $t\phi$ Einstein equation gives the *frame-dragging ODE* (Paper I):
$$
\frac{1}{r^4}\frac{d}{dr}!\left(r^4 j(r)\frac{d\omega}{dr}\right)

* \frac{4}{r}\frac{d\omega}{dr}=0,
  \qquad
  j(r)=e^{-\Phi(r)}\sqrt{1-\frac{2M(r)}{r}}.
  $$

Boundary conditions: regular at $r=0$; outside the star
$$
\omega(r)=\Omega-\frac{2J}{r^3},
$$
so matching at $r=R$ yields
$$
J=\frac{R^4}{6},\omega'(R),\qquad
\Omega=\omega(R)+\frac{2J}{R^3},
\quad
I\equiv\frac{J}{\Omega}.
$$

This is all you need to compute the **moment of inertia** to leading order. Do the TOV background first, then integrate $\omega$ once, then read off $J$ and $I$. (Paper IV generalizes energy relations and $I$ to **differential rotation**, with $M_{\rm rot}=\tfrac12 I\Omega^2 + \mathcal{O}(\Omega^4)$ for uniform rotation.)   

---

## 5) Second-order ($\ell=0$): spherical mass/pressure corrections

Rotation adds **centrifugal support**, shifting the enclosed mass and pressure spherically. Paper I writes coupled ODEs for $m_0(r)$ and $p_0^*(r)$ whose source terms involve $\bar{\omega}^2$:

* $m_0'(r)=4\pi r^2\frac{dE}{dP}(E+P),p_0^*(r) + \frac{1}{3}r^3\frac{d}{dr}!\bigl[r^2\bar{\omega}^2(r)\bigr]$,
* $p_0^*{}'(r)=-\Phi'(r)\frac{dE/dP}{E+P},p_0^*(r)-\frac{1}{3}\frac{r^3}{r-2M(r)},\bar{\omega}^2(r)$.

At the surface, the **mass increment** is
$$
\delta M = m_0(R) + \frac{J^2}{R^3},
$$
so $M_{\rm rot}=M+\delta M$. This is the number you compare across sequences when you talk about rotation-induced changes in stability thresholds. 

---

## 6) Second-order ($\ell=2$): quadrupolar shape and $Q$

The $\ell=2$ sector ($h_2,k_2,p_2^*$, etc.) yields the **oblateness** and the **mass quadrupole** $Q$. You solve another system of ODEs with sources $\propto p_2^*$ and $\bar{\omega}^2$. Matching at $r=R$ to the exterior vacuum solution fixes $Q$ from the $1/r^3$ part of $g_{tt}$ and $g_{rr}$’s $P_2(\cos\theta)$ terms; in practice $Q\sim -\mathcal{O}(J^2/M)$ for an oblate star. Paper I explicitly connects the GR result to **Clairaut’s equation** in the Newtonian limit—your cross-check when debugging $\ell=2$ numerics. 

---

## 7) What the later papers add (and why you care)

* **Paper II (models)**: integrates the above system for **realistic white-dwarf / neutron-star EOS** and for **$n=3$ polytropes** (supermassive stars), reporting $M$, $R$, $I$, $Q$, and surface flattening vs central density. Use it as a benchmark for your integrator and as a template for tables/plots.  

* **Paper III (static stability)**: extends the **turning-point criterion** to slow rotation. Roughly: along appropriate 2-parameter sequences (fixing $J$ or baryon number), the extrema of $M$ vs central density still flag where the **quasi-radial mode** goes marginal. The algebra shows how $\mathcal{O}(\Omega^2)$ shifts the critical density. 

* **Paper IIIA (correction)**: fixes a subtlety: properly compute the neutral mode when it **mixes with convective modes** in isentropic stars—this matters near marginal stability where naive non-degenerate perturbation theory fails. It clarifies how to construct the comparison sequence with the **correct differential rotation law**. If you skip this, you’ll get the wrong answer for the stability boundary.   

* **Paper IV (energy & $I$ for differential rotation)**: shows $M_{\rm rot}=\tfrac12!\int!\Omega,dJ$ for general slow **differential rotation**, reducing to $M_{\rm rot}=\tfrac12 I\Omega^2$ for rigid rotation. A clean variational argument; good for checking energy accounting without solving the full $\mathcal{O}(\Omega^2)$ system. 

* **Paper V ($n=3/2$ static stability)**: applies the static stability method to the **$n=3/2$ polytrope**, quantifies the (modest) stabilization from rotation, and demonstrates the full workflow end-to-end. Use it as a sandbox before you attempt fancy EOS. 

* **Paper VI (mode frequencies)**: derives formulas for the **rotation-induced shift** in quasi-radial mode frequencies to $\mathcal{O}(\Omega^2)$; necessary if you care about time-domain dynamics and GW damping of slowly rotating stars.  

* **Paper VIII (frequencies, $n=3/2$)**: evaluates Paper VI (and CF’s) expressions on the $n=3/2$ sequence and checks consistency—the two approaches agree. If your code reproduces this numeric, you’re on solid ground. 

---

## 8) Assumptions to keep straight (or you’ll chase ghosts)

* **Barotropic EOS $P=P(E)$**, isentropic; surfaces of constant $P$ and $E$ coincide. 
* **Rigid rotation** unless you’re explicitly in Paper IV’s setting.
* **Stationary, axisymmetric, equatorially symmetric**; no GW emission in equilibrium.
* **Slow rotation**: require
  $$
  \Omega^2 \ll \frac{M}{R^3}
  \quad\Rightarrow\quad
  v_{\rm eq}=\Omega R \ll c,
  $$
  so $\mathcal{O}(\Omega^3)$ terms are truly negligible in both geometry and fluid variables. 

---

## 9) Worked derivations you will actually use

### 9.1 Deriving TOV (sketch you can reproduce)

Start from $\nabla_\nu T^{\mu\nu}=0$ and the static metric above. The spatial ($\mu=r$) component gives the Euler equation in curved spacetime,
$$
\frac{dP}{dr}=-(E+P)\frac{d\Phi}{dr}.
$$
Combine with Einstein’s $G^r{}_r$ and $G^t{}_t$ to eliminate $\Phi'$ and identify $M(r)$; you land on **(TOV)** above. If your derivation doesn’t produce the $4\pi r^3P$ term, you missed curvature in the force balance.

### 9.2 Frame dragging and $I$ (first-order)

Insert the metric ansatz with $g_{t\phi}=-r^2\sin^2\theta,\omega(r)$ into the $t\phi$ Einstein equation and separate variables. You obtain the radial ODE in Section 4. Solve on $[0,R]$, match to $\omega=\Omega-2J/r^3$ outside, and read off $J$ and $I$. This is the cleanest moving part in the whole machinery; use it to validate your background model before touching $\ell=0,2$ sectors. 

### 9.3 Second-order spherical/quadrupolar ODEs

Vary the metric plus fluid to $\mathcal{O}(\Omega^2)$, decompose in Legendre $P_\ell$, and project Einstein’s equations on $\ell=0$ and $\ell=2$ pieces. Sources are built from $\bar\omega^2$ and EOS derivatives $dE/dP$. Integrate from $r=0$ with regularity, enforce $P(R)=0$ to fix the perturbed surface, and match $h_2,m_2$ to the exterior to extract $Q$. If your $Q$ sign flips without reason, you’ve likely mismatched gauge choices or boundary conditions. 

---

## 10) Notation and conventions (used across I–VIII)

| Symbol           | Meaning                                                                                               |
| ---------------- | ----------------------------------------------------------------------------------------------------- |
| $c=G=1$          | Geometric units throughout (restore units only at the end).                                           |
| $r$              | Schwarzschild (circumferential) radius.                                                               |
| $M(r),,M$        | Enclosed mass and total mass (non-rotating background).                                               |
| $R$              | Background radius ($P(R)=0$). In rotation, $R_{\rm eq}\neq R_{\rm pole}$ at $\mathcal{O}(\Omega^2)$.  |
| $E,,P,,N$        | Energy density, pressure, baryon number density; $P=P(E)$ (barotropic).                               |
| $\Phi(r)$        | Redshift potential with $g_{tt}=-e^{2\Phi}$.                                                          |
| $\Omega$         | Rigid angular velocity (asymptotic inertial frame).                                                   |
| $\omega(r)$      | Frame-dragging angular velocity; exterior $\omega=\Omega-\dfrac{2J}{r^3}$.                            |
| $\bar\omega(r)$  | $\Omega-\omega(r)$, fluid angular velocity relative to local inertial frames.                         |
| $I,,J$           | Moment of inertia and total angular momentum; $I=J/\Omega$.                                           |
| $h_0,m_0,k_0$    | $\ell=0$ metric perturbations ($\mathcal{O}(\Omega^2)$); $m_0(R)$ contributes to $\delta M$.          |
| $h_2,m_2,k_2$    | $\ell=2$ metric perturbations ($\mathcal{O}(\Omega^2)$); match to exterior to get $Q$.                |
| $p_0^*,,p_2^*$   | Dimensionless pressure perturbations multiplying $(E+P)$ in $\ell=0,2$ sectors.                       |
| $Q$              | Mass quadrupole; negative for oblate configurations ($\sim -J^2/M$ at slow rotation).                 |
| $M_{\rm rot}$    | Rotating mass; to $\mathcal{O}(\Omega^2)$, $M_{\rm rot}=M+\delta M$, with $\delta M=m_0(R)+J^2/R^3$.  |
| $T$              | Rotational energy; for rigid rotation $T=\tfrac12 I\Omega^2+\mathcal{O}(\Omega^4)$ (Paper IV).        |
| $\nu_{\rm mode}$ | Quasi-radial mode frequency; rotation shifts $\nu$ at $\mathcal{O}(\Omega^2)$ (Papers VI, VIII).      |

---

## 11) What “slow” really means (don’t hand-wave this)

Use a hard inequality, not vibes:
$$
\boxed{;\Omega^2 \ll \frac{M}{R^3};}
\quad \Longrightarrow \quad
\text{all } \frac{\delta g_{\mu\nu}}{g_{\mu\nu}},; \frac{\delta P}{P},; \frac{\delta E}{E}
= \mathcal{O}!\left(\frac{\Omega^2 R^3}{M}\right)\ll 1,
$$
and $v_{\rm eq}/c\ll1$. If those aren’t true, you’re out of the slow-rotation regime and should switch to a 2D rapid-rotation solver; pushing the Hartle–Thorne expansion past its domain won’t save you. 

---

## 12) Reading the series efficiently

1. **Implement** the TOV + frame-dragging solver and reproduce $I(M)$ and $\omega(r)$ matches.
2. **Add** the $\ell=0$ ODEs; recover $\delta M$ and compare to Paper II tables for a simple EOS.
3. **Add** the $\ell=2$ system; extract $Q$ and the surface flattening; sanity-check the Newtonian limit.
4. **For stability**, follow Paper III + IIIA’s corrected prescription (don’t skip IIIA).  
5. **For modes**, evaluate Paper VI’s frequency-shift functional and reproduce Paper VIII’s $n=3/2$ numerics.  

If a result disagrees, check (i) EOS units/scales, (ii) surface matching for $\omega$ and $\ell=2$ fields, (iii) whether you accidentally violated the slow-rotation bounds. Most “mystery” discrepancies turn out to be one of these.

---

### Appendix: surface matching identities you’ll reuse

At $r=R$,
$$
\omega(R^+)=\omega(R^-),\qquad
\omega'(R^+)=\omega'(R^-),\qquad
\omega(r!>!R)=\Omega-\frac{2J}{r^3}.
$$

For the $\ell=0$ mass correction,
$$
m_0(r>R)=\delta M - \frac{J^2}{r^3}.
$$

These two lines are workhorses for extracting $J$, $I$, and $\delta M$ from interior integrations. 

---

**Pointers to the series (for cross-checking derivations/tables):**

* Paper I: equations of structure to $\mathcal{O}(\Omega^2)$. 
* Paper II: models for realistic EOS and $n=3$ polytropes; exterior field notes. 
* Paper III / IIIA: static stability criterion and its correction.  
* Paper IV: rotational energy and $I$ with differential rotation. 
* Paper V: stability for $n=3/2$ polytropes. 
* Paper VI / VIII: quasi-radial mode frequency shifts and $n=3/2$ numerics.  
