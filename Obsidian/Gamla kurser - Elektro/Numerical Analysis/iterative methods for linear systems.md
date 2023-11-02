---
tags: [num]
aliases: [iterative solvers]
---
# Iterative methods for linear systems
When having a [[linear systems|linear system]] $Ax = b$ we will have some drawbacks using [[Gauss elimination|Gaussian elimination]]. The Gaussian is good in general but can give large:
- [[Tidskomplexitet|order notation]]
- [[memory]]
However, in application A is almost never completely "general",
we can do it more efficiently by using iterative methods ...

## [[fixed-point iterative methods]]

## [[splitting]]

## Choice of $x_{0}$ and P
- We need this guess to initiate "iterative solvers".
- $x_{0}$ can be arbitrary, however, [[convergence]] ([[fixed-point iterative methods]]) will be faster if we start with a good guess of the solution
- Choose P so that
		1. $Px_{k}=y$ is easy to solve $\longrightarrow \{ x_{1},x_{2},... \}$ is easily computed
		2. P approximates $A \longrightarrow \{ x_{1},x_{2},... \}$ converges rapidly 

