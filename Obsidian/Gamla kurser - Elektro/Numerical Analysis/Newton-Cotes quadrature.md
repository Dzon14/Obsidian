---
aliases: 
tags: [num]
---

# Newton-Cotes quadrature
Newton-Cotes quadrature is a family of numerical integration methods for approximating the definite integral of a function. These methods use equally spaced nodes and weights to construct a polynomial approximation of the integrand, which is then integrated exactly. The most basic Newton-Cotes method is the trapezoidal rule, which approximates the area under the curve by a trapezoid with the endpoints of the interval as the vertices. Other methods in the Newton-Cotes family include the midpoint rule, Simpson's rule, and the extended midpoint rule. These methods can be used for both closed and open intervals, and can be extended to higher dimensions for multiple integrals.

## [[trapezoidal rule]]

## [[Simpson's rule]]

## Open Newton-Cotes methods
The so-called closed Newton–Cotes Methods like Trapezoid and Simpson’s Rules require input values from the ends of the integration interval. Some integrands that have a removable singularity at an interval endpoint may be more easily handled with an open Newton–Cotes Method, which does not use values from the endpoints. The following rule is applicable to functions $f$ whose second derivative $f^{''}$ is continuous on $[a,b]$:

##### Midpoint rule
$$\int\limits_{x_{0}}^{x_{1}} f(x) \ dx = hf(w) + \frac{h^{3}}{24}f^{''}(c)$$where $h = (x_{1}-x_{0})$, $w$ is the midpoint $x_{0} + \frac{h}{2}$ and c is between $x_{0}$ and $x_{1}$.
- The Midpoint Rule is also useful for cutting the number of function evaluations needed. Compared with the Trapezoid Rule, the closed Newton–Cotes Method of the same order, it requires one function evaluation rather than two. Moreover, the error term is half the size of the Trapezoid Rule error term.

#### Composite midpoint rule
$$\int\limits_{a}^{b} f(x) \ dx = h \sum\limits_{i=1}^{m}f(w_{i})+ \frac{(b-a)h^{2}}{24}f^{''}(c)$$where $h= \frac{(b-a)}{m}$ and c is between a and b. The $w_{i}$ are the midpoints of the $m$ equal subintervals of $[a,b]$

## Example
![[Pasted image 20230428140012.png]]
