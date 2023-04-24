---
tags: [num]
aliases: [Gaussian quadrature]
---
# Gauss-Legendre quadrature
- The method is based on choosing a set of points, known as the Gauss-Legendre nodes, and a set of weights that correspond to the Legendre polynomials evaluated at these nodes.
- It uses orthogonal polynomials $P_{n}(x)$ of degree n  (Legendre polynomials) to approximate the integral of a function over a given interval.  They polynomials obey $$ \int\limits_{-1}^{1} P_{m}(x)P_n(x) \ dx = 0, \ \ \ if n \neq m$$
- It can be used when we want to find an optimal placements of nodes, where [[Newton-Cotes quadrature]] is not good enough. 

