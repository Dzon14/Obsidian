---
tags: [num]
aliases: [composite Newton-Cote]
---
# Composite quadrature
- Composite quadrature refers to a numerical integration technique in which an integral over a large interval is approximated by subdividing the interval into smaller subintervals and applying a numerical quadrature formula to each subinterval. The subintervals can have equal or different sizes, and the accuracy of the approximation can be improved by increasing the number of subintervals.
- The [[trapezoidal rule]] and [[Simpson's rule]] are limited to operating on a single interval. Of course, since definite integrals are additive over subintervals, we can evaluate an integral by dividing the interval up into several subintervals, applying the rule separately on each one, and then totaling up. This strategy is called composite numerical integration

![[Pasted image 20230405133835.png]]

## Composite quadrature
Splitting up the interval $[a,b]$ into N shorter sub-intervals $[a_{j},b_{j}], j = 1,...,N$, of length $h_{j}$. These sub-intervals are called *panels*. $$\int\limits_{a}^{b} f(x) \ dx = \int\limits_{a_{1}}^{b_{1}} f(x) \ dx + \int\limits_{a_{2}}^{b_{2}} f(x) \ dx, ..., + \int\limits_{a_{N}}^{b_{N}} f(x) \ dx$$with $a_{1}=a, b_{j}=a_{j+1}, b_{N}=b$, and apply the quadrature rule individually to each integral. 


## Composite [[Newton-Cotes quadrature]]
![[Pasted image 20230405134049.png]]

## Composite [[trapezoidal rule]]
$$\int\limits_{a}^{b} f(x) \ dx = \frac{h}{2} \left( y_{0}+y_{m}+ 2 \sum\limits_{i=1}^{m-1}y_{i} \right) - \frac{(b-a)h^{2}}{12}f^{''}(c)$$where $h = \frac{b-a}{m}$ and $c$ is between $a$ and $b$.


## Composite [[Simpson's rule]]
![[Pasted image 20230405134640.png]]
From book: $$\int\limits_{a}^{b} f(x) \ dx = \frac{h}{3} \left[ y_{0}+y_{2m} + 4 \sum\limits_{u=1}^{m}y_{2i-1} + 2 \sum\limits_{u=1}^{m-1}y_{2i}  \right] - \frac{(b-a)h^{4}}{180}f^{(iv)}(c)$$where c is between a and b.

## Illustrations
![[Pasted image 20230421151735.png]]

## Example from book
