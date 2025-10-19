
# Paper III — Static Criterion for Stability (Hartle & Thorne 1969)

**PDF:** [III.pdf](sandbox:/mnt/data/III.pdf)

## Objective
Generalize the **turning-point stability criterion** (for non-rotating stars) to **slowly and rigidly rotating** configurations. Identify how $\mathcal{O}(\Omega^2)$ effects shift the **critical central density** at which a quasi-radial mode becomes unstable.

## Background
- Non-rotating case: maxima/minima on $M(E_c)$ (or binding energy vs. $E_c$) curve typically signal **neutral stability** for radial modes.  
- Rotating case adds a second parameter $J$ (or $\Omega$). The family is now 2D: $(E_c, J)$.

## Strategy
Construct **constant-$J$ (or constant baryon number)** sequences and examine **extrema** in $M$ vs. $E_c$ along those sequences. Show that (to $\mathcal{O}(\Omega^2)$) these extremal points still diagnose the onset of quasi-radial instability—i.e., where the squared frequency passes through zero.

## Main Statement (schematic)
If $E_{cc}$ is the non-rotating critical central density, then
```math
E_{cc}(\text{rot}) = E_{cc} + \epsilon_{cc}(J),
\quad \epsilon_{cc}(J)=\mathcal{O}(J^2),
```
with $\epsilon_{cc}$ computable from the **difference in masses** between the uniformly rotating sequence and a carefully constructed **comparison sequence** (see Paper IIIA).

## Mathematical Content
- Use the Paper I **mass correction** $\delta M$ and the **first-order** $I$ to express $M(E_c,J)$ to $\mathcal{O}(J^2)$.  
- Show that extrema of $M$ along constant-$J$ (or constant baryon) curves coincide with **neutral modes** of the quasi-radial spectrum (to this order).  
- No need to solve full pulsation ODEs to diagnose **stability boundaries**.

## Physical Meaning
Rotation slightly **stabilizes** stars against collapse (shifts the critical point), but to leading order the **turning-point logic survives**: maxima/minima still flag the change in stability.

## Caveats
- Requires the **correct comparison sequence** for differential rotation induced by a neutral mode—this is corrected in **Paper IIIA**.  
- Assumes barotropic EOS and slow rotation.  
