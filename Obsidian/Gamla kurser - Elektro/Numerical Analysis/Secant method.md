---
tags: [num]
---
# Secant Method
The Secant Method is similar to the Newton’s Method, but replaces the derivative by a difference quotient. Geometrically, the tangent line is replaced with a line through the two last known guesses. The intersection point of the “secant line’’ is the new guess.
- Two starting guesses are needed - $x_{0}, x_{1}$
$$x_{i+1}=x_{i}- \frac{f(x_{i})(x_{i}-x_{i-1})}{f(x_{i})-f(x_{i-1})}$$
The rate of convergence is $p \approx 1.62$ (*super-linear*) for a single root
Compare with fixed point (p=1) and [[Newton's method]] (p=2)

The advantage of not having to compute a derivative is countered by having a slower convergence rate.

## Example from book
![[Pasted image 20230421133851.png]]

## Method of false positioning (in course??)
There are three generalizations of the Secant Method that are also important. The Method of False Position, or Regula Falsi, is similar to the Bisection Method, but where the midpoint is replaced by a Secant Method–like approximation.
![[Pasted image 20230421134003.png]]

#### Example
![[Pasted image 20230421134017.png]]