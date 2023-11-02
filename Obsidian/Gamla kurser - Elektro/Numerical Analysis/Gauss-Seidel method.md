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
1. $(L+D)x_{k+1}=y$ is easy to solve ([[triangular matrix|lower triangular]])
2. $(L+D)$ approximates $A$ (better than just $D$ as in the jacobi method)

- If $\lvert \lvert B \rvert \rvert<1$ it converges

**Theorem**
If $A\in\mathbb{R}^{n\times n}$ is strictly diagonally dominant, then for nay $b\in\mathbb{R}^{n}$ and $x_{0}\in\mathbb{R}^{n}$ (starting value) the Gauss-Seidel method converges to a solution of $Ax=b$.

## Härledning
$A=L+D+U$ (as for [[Jacobi method]]) gives $(L+D+U)x = b$. This gives $$\begin{align} &(L+D)x = -Ux + b \\ &x= (L+D)^{-1}(-Ux+b) \\ &x_{k+1} = (L+D)^{-1}(b-Ux_{k}) = x_{k+1}=\underbrace{ -(L+D)^{-1}U }_{ =B }x_k+\underbrace{ (L+D)^{-1}b }_{ =c }\end{align}$$ $i=0,1,...$
## Gauss-Seidel with twist
From the standard formula above we can write $$\begin{align} &Lx_{k+1} + Dx_{k+1}= b-Ux_{k} \\ &Dx_{k+1}=b-Ux_{k}-Lx_{k+1} \\ &x_{k+1}=D^{-1}(b-Ux_{k}-Lx_{k+1}) \end{align}$$$i=0,1,...$
This formula is equivalent to the "standard" formula, but it looks a bit funny. Could one really have $x_{i+1}$ on the right hand side of an iterative formula? The answer is “yes”. The explanation is that matrix-vector multiplication on the right hand side of this formula is done one row at a time, thereby producing the new entries of $x_{i+1}$ one by one – starting at the top. Thanks to the strictly lower triangular structure of $L$, the individual entries of $x_{i+1}$ on the right hand side are only needed in $Lx_{i+1}$ when they already have been produced.

## Example
![[Pasted image 20230327161015.png]]
![[Pasted image 20230327161027.png]]

## Example from book
![[Pasted image 20230330132059.png]]![[SmartSelect_20230418_113455_Samsung Notes.jpg]]
