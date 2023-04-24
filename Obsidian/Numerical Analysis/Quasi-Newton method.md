---
tags: [num]
---
# Quasi-Newton Method
The Quasi-Newton method is a numerical optimization algorithm used to find the minimum or maximum of a function. It is an iterative method that is similar to Newton's method, but instead of computing the Hessian matrix (the matrix of second derivatives of the function), it approximates it using information from previous iterations. The Quasi-Newton method is useful when the Hessian matrix is too difficult or expensive to compute directly. There are several variations of the Quasi-Newton method, such as the Broyden-Fletcher-Goldfarb-Shanno (BFGS) method and the Davidon-Fletcher-Powell (DFP) method, which differ in how they update the approximation to the Hessian matrix.


A typical step looks like:
- Compute $d^{(k)} := -H^{(k)}f(x^{(k)})$
- Compute $x^{(k+1)}:= x^{(k)} +d^{(k)}$
- Update by some method $H^{(k)} \rightarrow H^{(k+1)}$

## See [[Broyden condition]]
