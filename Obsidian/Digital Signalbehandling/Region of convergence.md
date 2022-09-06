---
aliases: [ROC]
---

# Region of convergence (Convergence of X(z))
**ROC** - region of convergence 
- The ROC of X(z) is all z values for which it attains a finite value. $$ROC:ALL \ z \in \mathcal{C} \ for \ which \ \lvert x(z)\rvert < \infty$$
- Important to be aware of the ROC when working with the Z-transform. 
- Expressing z in polar form can help perform an analysis of an arbitrary sequence/signal.
- To identify the corresponding sequence/signal we need to know **both** the z-transform and its ROC

### Finding the ROC
- Express the sequence in polar form
- Find out when $\lvert X(z) < \infty \rvert$ 
- The total ROC will be the intersection of a sum depending on an anti-casual part of the sequence and a sum depending on a causal part. 
- If both these sums are **finite**, we are inside the **ROC**. 
![[Pasted image 20220905133849.png|400]]
where $S_1$ is the anti-causal and $S_2$ is the causal.
**See** [[Kausalitet|causality]]. for def: for causal and anti-causal.

### Two-sided
![[Pasted image 20220905134751.png|800]]

### Characteristic ROC shapes
![[Pasted image 20220905134833.png|650]]


#el