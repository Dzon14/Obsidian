---
tags: [num]
---
# Secant Method
The Secant Method is similar to the Newton’s Method, but replaces the derivative by a difference quotient. Geometrically, the tangent line is replaced with a line through the two last known guesses. The intersection point of the “secant line’’ is the new guess.
- Two starting guesses are needed
$$x_{k}=x_{k-1}- \frac{f(x_{k-1})(x_{k-1}-x_{k-2})}{f(x_{k-1})-f(x_{k-2})}$$
The rate of convergence is $p \approx 1.62$ (*super-linear*) for a single root
Compare with fixed point (p=1) and [[Newton's method]] (p=2)

The advantage of not having to compute a derivative is countered by having a slower convergence rate.