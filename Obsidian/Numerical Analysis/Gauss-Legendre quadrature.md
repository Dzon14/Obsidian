---
tags: [num]
aliases: [Gaussian quadrature]
---
# Gauss-Legendre quadrature
- The method is based on choosing a set of points, known as the Gauss-Legendre nodes, and a set of weights that correspond to the Legendre polynomials evaluated at these nodes.
- It uses orthogonal polynomials $P_{n}(x)$ of degree n  (Legendre polynomials) to approximate the integral of a function over a given interval.  They polynomials obey $$ \int\limits_{-1}^{1} P_{m}(x)P_n(x) \ dx = 0, \ \ \ if \ \ n \neq m$$
- It can be used when we want to find an optimal placements of nodes, where [[Newton-Cotes quadrature]] is not good enough. 
- The degree of precision of a quadrature method is the degree for which all polynomial functions are integrated by the method with no error. Newton–Cotes Methods of degree n have degree of precision n (for n odd) and n + 1 (for n even). The [[trapezoidal rule]] ([[Newton-Cotes quadrature]] for n = 1) has degree of precision one. [[Simpson's rule]] (n = 2) is correct up to and including third degree polynomials. To achieve this degree of precision, the Newton–Cotes formulas use n + 1 function evaluations, done at evenly spaced points. The question we ask is reminiscent of our discussion in Chapter 3 about Chebyshev polynomials. Are the Newton–Cotes formulas optimal for their degree of precision, or can more powerful formulas be developed? In particular, if the requirement that evaluation points be evenly spaced is relaxed, are there better methods? At least from the point of view of degree of precision, there are more powerful and sophisticated methods. We pick out the most famous one to discuss in this section. Gaussian Quadrature has degree of precision 2n + 1 when n + 1 points are used, double that of Newton–Cotes. The evaluation points are not evenly spaced.
- It has a precision of $2n-1$ (using n Legendre polunomial on $[-1,1]$)

## Definition and Theorem - orthogonal
![[Pasted image 20230429184608.png]]
##### Example
![[Pasted image 20230429184808.png|500]]
![[Pasted image 20230429184829.png]]

## Gaussian Quadrature - Formula
$$\int\limits_{-1}^{1} f(x) \ dx \approx \sum\limits_{i=1}^{n} c_{i}f(x_{i})$$where $$c_{i}= \int\limits_{-1}^{1} L_{i}(x) \ dx, \ \ \ \ i=1, \dots , n$$The $c_{i}$ are tabulated to great accuracy. Values are given in table below, up to $n=4$
![[Pasted image 20230429185214.png|600]]

## Example
![[Pasted image 20230429185329.png]]


