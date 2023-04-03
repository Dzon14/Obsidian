---
aliases: [Gausselimination, Gausseliminering, Gaussian elimination]
tags: [num]
---
# Gauss elimination
- In numerical analysis: Gaussian elimination is a finite sequence of $\mathcal{O}(n^{3})$ floating point operations that result in a solution. For that reason, Gaussian elimination is called a *direct* method for solving systems of linear equations. Direct methods, in theory, give the exact solution within a finite number of steps.

Two [[linear systems]] are *equivalent* if and only if they have the same solution set.
The following operations give an equivalent system:
- Interchange
- Scaling
- Replacement

- Use tableau form

![[Pasted image 20230321162302.png]]
- Solve by using [[back substitution]]

## [[pivoting]]

## Operation count of Gauss...
$$\frac{2}{3}n^{3} + \frac{3}{2}n^{2} - \frac{7}{6} n$$

## Numerical implementation
![[Pasted image 20230326132429.png]]

## Drawbacks
- Algorithm only provides theoretically the exact solution x
- Rounding errors lead practivally to an approximation $\tilde{x} \in \mathbb{R}^{n}$
- The quality of the approximation depends on the condition of A
- The computational complexity of Gaussian elimination is cubic (O($n^{3}$)) for full matrices
- For [[sparsity|sparse matrix]] Gaussian may lead to full triangular matrices (fill-in effect).