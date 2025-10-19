
# Paper V — Static Stability Analysis of $n=3/2$ Polytropes (Hartle & Munn 1975)

**PDF:** [V.pdf](sandbox:/mnt/data/V.pdf)

## Objective
Concrete application of the **static stability method** (Papers III & IIIA) to the **$n=3/2$ Tooper polytrope** (roughly $\gamma=5/3$; toy model for nonrelativistic degeneracy). Quantify the **rotation-induced** shift of the stability boundary and test the full workflow.

## Method Outline
1. Choose EOS: $n=3/2$ relativistic polytrope.  
2. Build non-rotating sequences $M(E_c)$ (TOV). Identify non-rotating **turning points**.  
3. Incorporate slow uniform rotation (Paper I) $\Rightarrow$ compute $J$, $I$, and $\delta M$.  
4. Construct the **comparison sequence** with the **correct (IIIA) differential rotation** induced by the neutral mode.  
5. Use the **mass-equality** condition to determine the **shift** in the critical central density $E_{cc}(J)$.

## Results (Qualitative)
- Rotation **stabilizes** the polytropic sequence slightly (critical density increases/decreases depending on definition; boundary shifts at $\mathcal{O}(J^2)$).  
- The size of the shift depends on compactness and EOS stiffness; for $n=3/2$ the effect is measurable but modest in the strict slow-rotation domain.

## Deliverables
- **Numerical tables/curves**: $M(E_c)$, stability boundaries vs $J$; cross-checks against Paper III/IIIA formalism.  
- A worked example to validate your implementation before tackling realistic EOS.

## Takeaway
Paper V is your **sandbox**: reproduce these results to ensure your static stability pipeline is correct, including the IIIA correction.
