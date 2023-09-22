---
tags: [num]
---
# Simpson's rule
- An another form of [[Newton-Cotes quadrature]] that uses quadratic polynomials to approximate the integrand over each subinterval, resulting in a more accurate approximation of the integral compared to the [[trapezoidal rule]]
- Similar to the [[trapezoidal rule]] except that the degree 1 interpolant is replaced by a parabola - $Q^{2}$

## Formula - book
$$\int\limits_{x_{0}}^{x_{2}} f(x) \ dx = \frac{h}{3} (y_{0}+4y_{1}+y_{2})- \frac{h^{5}}{90}f^{''''}(c)$$where $h=x_{2}-x_{1}=x_{1}-x_{0}$ and $c$ is between $x_{0}$ and $x_{2}$.


![[Pasted image 20230404162800.png]]

## Change of interval - Transformation theorem
![[Pasted image 20230404162917.png]]

## Error
From book: $$\int\limits_{x_{0}}^{x_{2}} E(x) \ dx = - \frac{h^{5}}{90}f^{('''')}(c)$$
for some interval $c \in [x_{0},x_{2}]$.
From lecture notes it is: $$\lvert I-I_\approx = \frac{\left\lvert f^{''''}(c) \right\rvert}{2880} \rvert h^{5}$$for some $c \in [a,b]$

## Illustration
![[Pasted image 20230404173428.png]]

## Example from book 
![[Pasted image 20230421150832.png]]
![[Pasted image 20230421150846.png]]