---
tags: [num]
---
# Modified Newton's Method
- An extension of [[Newton's method]] for finding the roots of [[nonlinear equation|nonlinear equations]]
- Modifies the standard method when it fails to [[convergence|converge]] or does it too slowly. 
- This modification can be done in several ways, such as using a different initial guess, changing the updating formula, or using a damping factor to reduce the step size. The goal is to improve the convergence properties of the standard method while maintaining the same order of convergence
- A downside could be that it requires more iterations or additional computations. 

## Formula 
Using a multiplicator m:
$$x_{k+1}=x_{k}-m \frac{f(x_{k})}{f'(x_{k})}$$![[Pasted image 20230403165733.png|350]]

## Theorem 
If $f : [a,b] \rightarrow \mathbb{R}$ is $(m+1)$-times continously differentiable and has root $r \in [ a,b]$ with multiplicy $m>1$, then *Modified Newton's Method* converges localy and quadratically to r. 

## Another way: [[damped Newton method]]


