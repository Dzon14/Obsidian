---
aliases: [fixed-point iterative method]
---

# fixed-point iterative methods
A class of iterative methods for [[linear systems]].
The idea is to rewrite $Ax=b$ into $$x= Bx +c$$By doing a initial gauess $x_{0}$ and
Given $x_{0} \in \mathbb{R}^{n}$ we construct $$x_{k+1} = Bx_{k}+c \ \ \ \ k=0,1,...,$$so that a fixed point of $g(x) = Bx+c$ is a solution of $Ax =b$
*Iteration error:* $e_{k}=x_{k}-k$

The iterative method is [[convergence|convergent]] (fixed-point iterative methods) if $$\lim_{k\to \infty }e_{k}= 0$$for any choice of $x_{0} \in \mathbb{R}^{n}$
Efficient for very large sparse systems
- Also called *indirect* methods (where [[Gauss elimination]] and [[LU factorization|LU]] are direct methods)

## Convergence

![[Pasted image 20230327153701.png]]$$ \lvert \lvert e_{k+1} \rvert \rvert \leq \lvert \lvert B \rvert \rvert^{k+1} \lvert \lvert e_{0} \rvert \rvert \rightarrow 0 \text{ as } k \rightarrow 0 \text{ if } \lvert \lvert B \rvert \rvert < 1$$The smaller $\lvert \lvert B \rvert \rvert$ is, the faster is the convergence/fixed-point iterative method.

## The simplest method: [[Jacobi method]]

## more efficient method: [[Gauss-Seidel method]]