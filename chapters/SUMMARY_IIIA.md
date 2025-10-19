
# Paper IIIA — The Static Stability Criterion Recovered (Hartle 1975)

**PDF:** [IIIA.pdf](sandbox:/mnt/data/IIIA.pdf)

## Why this paper?
Paper III’s construction of the **comparison sequence** (used to locate the neutral mode) had a flaw: in the Newtonian limit it did **not** enforce that the **induced differential rotation** be constant on cylindrical shells for isentropic stars. Paper IIIA fixes this and gives the **correct** prescription in full GR.

## Core Idea
A neutral (zero-frequency) mode at the stability boundary **conserves local angular momentum** of fluid elements. That conservation law **induces a specific differential rotation** profile when you displace the uniformly rotating star along the neutral mode. The comparison sequence must **exactly** implement this profile to ensure the mass equality used to solve for the stability shift is correct.

## Formal Statement
Let $M_u(E_c,J)$ be the mass of the **uniformly rotating** sequence, and $M_d(E_c,J,\delta E_c)$ the mass of the **differentially rotating** comparison sequence produced by the neutral-mode displacement labeled by $\delta E_c$. Neutral stability implies
```math
M_d(E_{cc}+\delta E_c, J, \delta E_c) = M_u(E_{cc}, J) + \mathcal{O}(J^3).
```
Solving this to $\mathcal{O}(J^2)$ yields the **rotation-induced correction** to the critical central density.

## What Changes vs Paper III
- The induced $\\,\delta\\Omega\\,$ is computed from **local angular-momentum conservation** (mixing between the neutral radial mode and **neutral convective modes** in isentropic stars).  
- The corrected comparison sequence ensures proper **cylindrical-shell constancy** in the Newtonian limit, and the fully relativistic generalization obeys the same physics.

## Outcome
With the corrected differential rotation law, the **static stability criterion** for slowly rotating stars is **recovered**: you can determine the stability boundary from equilibrium sequences **without** solving full pulsation equations, provided you use the **right** comparison sequence.

## Practical Guidance
- When reproducing stability boundaries: implement the Paper IIIA comparison sequence, **not** the naive one from III.  
- Expect small $\mathcal{O}(J^2)$ shifts in $E_{cc}$; sign and magnitude depend on EOS stiffness and compactness.  
