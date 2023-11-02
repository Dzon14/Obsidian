---
tags: [num]
aliases: [quadrature]
---
# Numerical Integration
- A technique to approximate the value of a definite integral of a function. It involves dividing the area under the curve into a finite number of smaller regions and then approximating the area of each region using a suitable formula. The approximated areas are then summed up to obtain an approximation of the integral value. There are several numerical integration methods, including the trapezoidal rule, Simpson's rule, and Gaussian quadrature, among others. These methods differ in the level of accuracy, complexity, and applicability to different types of integrals.
- That a integral can be evaluated via a primitive function in closed form is wrong (In numerical analysis).
- The vast majority of all integrations that take place in the world is done numerically and they follow *quadrature rules* (methods).
- These methods can be expressed as a Riemann sum $$I \equiv \int\limits_{a}^{b} f(x) \ dx \approx I_{app} \equiv \sum\limits_{i=0}^{n}f(x_{i})w_{i}$$Here the $n+1$ points $x_{i} \in [a,b]$ are (pairwise disjoint) *nodes* where the integrand $f(x)$ is sampled and the $n+1$ numbers $w_{i}$ are [[weight|weights]] which attach widths $\Delta x_{i} = w_{i}$ to the samples $f(x_{i})$.
- $I_{D} = Q^N_{D}$ 
- $f(x_{i}) = f(x_{n})$

## How to find nodes and weights
A common way to construct quadrature rules is to use a combination of [[interpolation]] and analytic integration. Through [[Lagrange interpolation]] we can derive the choice of weights:
$$w_{i}=\int\limits_{a}^{b} \phi_{i}(x) \ dx$$
- Quadrature rules derived with Lagrange using equidistant nodes are called [[Newton-Cotes quadrature]] rules.
		- Useful for ex. when integratind data measured at regularly recurring times. 
- [[Gauss-Legendre quadrature]] uses non-equidistant spacing for the nodes, which is more efficient if the circumstances permit such spacing.

## [[composite quadrature]]

## Different types of quadratures
- [[Newton-Cotes quadrature]]
- [[adaptive quadrature]]
- [[Gauss-Legendre quadrature]]
- [[composite quadrature]]


## Change of integration interval 
Assume n+1 canonical nodes and weights $\{ x_{i},w_{i} \}$ so that $$ \int\limits_{-1}^{1} f(x) \ dx \approx \sum\limits_{i=0}^{n}f(x_{i})w_{i}$$where $f(x)$ is a smooth function. *How* do we find a set of nodes and [[weight|weights]] $\{ y_{i}, w_{i}^{*} \}$ suitable for integration of another smooth function $g(y)$ on another intervall $[a,b]$? $$\int\limits_{a}^{b} g(y) \ dy \approx \sum\limits_{i=0}^{n}g(y_{i})w_{i}^{*}$$Answer is to start with variable change $$y = \frac{a+b}{2}+ \frac{b-a}{2}x \ \Rightarrow \ dy = \frac{b-a}{2}dx$$ which maps $x=-1$ to a and $x=1$ to b. Then we get $$\begin{align} \int\limits_{a}^{b} g(y) \ dy = \int\limits_{-1}^{1} g \left(\frac{a+b}{2}+ \frac{b-a}{2}x \right)  \ \frac{ b-a}{2}dx  \\  \approx \sum\limits_{i=0}^{n}g \left( \frac{a+b}{2} + \frac{b-a}{2}x_{i} \right) \frac{b-a}{2}w_{i} \end{align}$$From this we can see $$y_{i} = \frac{a+b}{2}+ \frac{b-a}{2}x_{i}, \ \ \ w_{i}^{*}= \frac{b-a}{2}w_{i}, \ \ \ i = 0,1,...,n$$