---
tags: [num]
---
# Cubic spline interpolation
- we can't always rely on [[polynomial interpolation]], since we don't always know that data points comes from a function resembling a polynomial.
- When there is uncertainty about what type of function underlies the data points, a piecewise polynomial interpolation scheme known as cubic splines is very popular
- A type of [[piecewise polynomial interpolation]]
- The idea is to use interpolating polynomials of degree three on each consecutive interval $[x_{i},x_{i+1}]$. That is, on the first interval $[x_{0},x_{1}]$ we seek the polynomial $$S_{1}(x) = a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}$$and on the second interval $[x_{1},x_{2}]$ we seek another polynomial $$S_{2}(x) = b_{0}+b_{1}x+b_{2x^2}+b_{3}x^{3}$$and so on..
- We use this to get  a smoother curve
![[Pasted image 20230329161759.png|500]]

![[Pasted image 20230328165207.png]]

## Existence of cubic splines
- **Property 1**: $S_{i}(x_{i-1}) = f_{i-1},(1 \leq i \leq N) \Rightarrow a_{i}=f_{i-1}$
- **Property 2**: $S_{i}(x_{i}) = f_{i}, (1 \leq i \leq N)$
- **Property 3**: $S_{i}^{(k)}(x_{i}) = S_{i+1}^{k}(x_{i})$ for $i = 1,...,N-1, \ k=1,2$
Total number of conditions to be fulfilled: $2N+2(N-1) = 4N-2$
Total number of coefficients (unknowns) to be determined: 4N $\Rightarrow$ 2 *degrees of freedom*

## Properties from book
![[Pasted image 20230329161945.png|650]]

## Types of cubic splines
- **Natural** cubic [[spline]]: $S''(x_{0}) = 0$ and $S''(x_{N}) = 0$
- **Clamped** cubic [[spline]]: $S_{1}'(x_{0}) =v_{0} \in \mathbb{R}$ and $S_{N}'(x_{N}) =v_{N} \in \mathbb{R}$
- **Curvature-adjusted** cubic [[spline]]: $S_{1}''(x_{0}) = v_{0}$ and $S_{N}''(x_{N}) = v_{N}$
- **Not-a-knot** cubic [[spline]]: $S_{1}'''(x_{1})=S_{2}'''(x_{1})$ and $S_{N-1}'''(x_{N-1}) = S_{N}'''(x_{N-1})$
		  - (This is [[matlab]]s default when using the spline command)

## Example from book
Check that properties are satisfied for ![[Pasted image 20230418150306.png]]
![[Pasted image 20230418150320.png]]

## Another example
![[Pasted image 20230418151316.png]]
![[Pasted image 20230418151326.png]]
![[Pasted image 20230418151345.png]]