---
tags: [num]
---
# Broyden condition
- The Broyden condition is a condition that ensures that the inverse Jacobian approximation in a [[Quasi-Newton method]] remains positive definite. It states that the change in the approximation of the inverse Jacobian must satisfy a ceratin equation that preserves the positive definiteness of the matrix. Specifically, the Broyden condition requires that the change in the inverse Jacobian approximation must be a rank-1 update, where the rank-1 update is constructed to preserve the positive definiteness of the approximation. The Broyden condition is important for ensuring the stability and convergence of quasi-Newton methods.
- If we have a inverse of a matrix we can get the inverse of another ???? (since it's rank 1????) (sherman- morrison)

![[Pasted image 20230403180314.png]]

## Sherman - Morrison (Woodbury) formula
![[Pasted image 20230403180346.png]]
- We do not have to know this formula for exam ..

## Simple Rank-1 update
![[Pasted image 20230403180400.png]]