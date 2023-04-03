---
tags: [num]
aliases: [interpolation errors]
---
# Interpolation error
- In numerical analysis, interpolation error refers to the difference between the actual function value and the interpolated value at a specific point. When approximating a function using an interpolation method, the interpolated value may differ from the actual value due to the nature of the approximation.

![[Pasted image 20230328161032.png]]
- We can also write P-f and positive right side
- $N=D-1$

## Error estimate
From $I = [a,b] \Rightarrow \lvert x-x_{i} \rvert \leq b - a$, as $x, x_{i}\in I$ $$\Rightarrow \lvert \lvert B_{N+1} \rvert \rvert_{\infty}\leq(b-a)^{N+1}$$
- If $b-a \leq 1$ : then $\lvert \lvert B_{N+1} \rvert \rvert_{\infty}\leq 1$ (bounded)
- if $b-a <1$ : then $\lvert \lvert B_{N+1} \rvert \rvert_{\infty}\leq(b-a)^{N+1} \rightarrow 0 \text{ for } N \rightarrow \infty$
- In general $\lvert \lvert B_{N+1} \rvert \rvert_{\infty}\rightarrow \infty$

## Example - values of $\lvert \lvert B_{N+1} \rvert \rvert_\infty$ : Equidistant points
![[Pasted image 20230328161552.png]]

## Placement of interpolation points
Does the error decrease as the degree of the polynomial increases?
- YES: if the points are *well-chosen*
- NO: in some cases, the error gets larger as $N \rightarrow \infty$

## How to reduce the error by minimixing $\lvert \lvert B_{N+1} \rvert \rvert_\infty$
- [[Chebyshev interpolation]]