---
tags: [num]
---
# Condition number

### Definition
Let $A \in \mathbb{R}^{nxn}$ be regular. The *condition number* of A with respect of the [[vector norm|p-norm]] is defined by $$\kappa_{p}(A) = \lvert \lvert A \rvert \rvert_{p}\lvert \lvert A^{-1} \rvert \rvert_{p}$$
## Floating point
In the floating point arithmetic, the relative [[backward & forward error|backward error]] cannot be expected to be less than $\epsilon_{mach}$, as storing the entries of b will already cause errors of that size.
![[Pasted image 20230322165208.png]]

## Properties 
![[Pasted image 20230322165320.png]]
- $\kappa(A)_{p} \approx1$ : well conditioned
- $\kappa_{p}(A) > 10^{8}$ : ill-conditioned
- $\kappa_{p}(A) > 10^{16}$ : completely unreliable