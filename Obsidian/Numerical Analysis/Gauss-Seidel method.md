---
tags: [num]
---
# Gauss-Seidel method
- A more efficient [[fixed-point iterative methods|fixed-point iterative method]] than [[Jacobi method]].
- The only difference between Gauss–Seidel and Jacobi is that in the former, the most recently updated values of the unknowns are used at each step, even if the updating occurs in the current step.
- If compared with (last) example in [[Jacobi method]] , Gauss-Seidel instead look like this:  
![[Pasted image 20230330112842.png]]

In general we have the formula:$$(L+D)x^{(k)} = -Ux^{(k-1)} + b$$
## Convergence theorem
If the $n \times n$ matrix A is strictly diagonally dominant, then (1) A is a nonsingular matrix, and (2) for every vector b and every starting guess, the Gauss–Seidel Method applied to $Ax = b$ converges to a solution.

## In matrix form
The gauss-seidel method is a fixed-point iterative method for solving linear systems, based on the jacobi method.

$$
P=L+D \Rightarrow N=-U
$$
$$
x_{k+1}=\underbrace{ -(L+D)^{-1}U }_{ =B }x_k+\underbrace{ (L+D)^{-1}b }_{ =c }
$$
1. $(L+D)x_{k+1}=y$ is easy to solve ([[Triangular Matrix|lower triangular]])
2. $(L+D)$ approximates $A$ (better than just $D$ as in the jacobi method)

- If $\lvert \lvert B \rvert \rvert<1$ it converges

**Theorem**
If $A\in\mathbb{R}^{n\times n}$ is strictly diagonally dominant, then for nay $b\in\mathbb{R}^{n}$ and $x_{0}\in\mathbb{R}^{n}$ (starting value) the Gauss-Seidel method converges to a solution of $Ax=b$.


## Example
![[Pasted image 20230327161015.png]]
![[Pasted image 20230327161027.png]]

## Example from book
![[Pasted image 20230330132059.png]]