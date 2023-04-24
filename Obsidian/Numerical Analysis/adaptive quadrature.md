---
tags: [num]
---
# Adaptive (composite) quadrature
- A [[numerical integration]] method used to approximate the definite integral of a function over a given interval. 
- The method involves dividing the interval into smaller subintervals (composite) and approximating the integral over each subinterval using quadrature rule, such as [[trapezoidal rule]] or [[Simpson's rule]].
- The key feature of adaptive quadrature is that it uses an iterative process to refine the subintervals based on the error estimate of the quadrature rule used. If the error estimate of a subinterval is above a given tolerance level, the subinterval is subdivided into smaller subintervals, and the quadrature rule is applied again to the new subintervals. This process continues until the error estimate for all subintervals is below the tolerance level.
- Useful in cases where the function being intergrated is complex or where the integrand varies rapidly over the integration interval. 

![[Pasted image 20230405101119.png]]
For ex. this graph shows a function that varies rapidly around $x=1$. We must choose extremely small panels $\Gamma_{j}$ to capture these variations. The basic strategy that all adaptive solvers use is the following, where $I_{j}$ is the exact value of the integral on a panel $\Gamma_{j}$ and $I_{app,j}$ is the numerical approximation obtained with the underlying quadrature rule used:
1) Choose a tolerance *tol*
2) Divide $[a,b]$ into a small number $N$ of panels $\Gamma_{j}, \ j = 1,2,...,N.$ This is called the original *mesh*
3) Construct a loop where the panels $\Gamma_{j}$ of the mest are processed, one after the other, according to step 4) and step 5) below
4) Compute $I_{app,j}$, then subdivide $\Gamma_{j}$ into two equisized panels $\Gamma_{j1}$ and $\Gamma_{j2}$ and also compute $I_{app,j1}$ and $I_{app,j2}$.
5) If it holds on $\Gamma_{j}$ that $$\lvert I_{app,j}- (I_{app,j1}+I_{app,j2}) \rvert \leq tol$$then accept $I_{app,j}$ as an approximation to $I_{j}$ and continue with step 3) for $\Gamma_{j+1}$. If the equation above doesn't hold, then *refine* the mesh with one panel by renumbering so that $\Gamma_{k}=\Gamma_{k-1}$ for $k \geq j+2, \ \Gamma_{j+1} = \Gamma_{j2}, \Gamma_{j1},$ and continue with step 3) for $\Gamma_{j}$.
6)  When all panels on the refined mesh have been processed, compute $$I_\approx= \sum\limits_{j}^{}I_{app,j}$$
   **Two remarks:**
   First, since $I_{app,j1}+I_{app,j2}$ must be a better approximation to $I_{j}$ than $I_{app,j}$, one redefines $I_{app,j}$ in the equation above as $I_{app,j1}+I_{app,j2}$. Secondly, there is no guarantee for a specific global accuracy. The tolerance tol only controls the local error.

## Numerical example
See lecture8.m for approximarion of $$f(x) = \begin{cases} 1, \ \ \ &x \leq 0 \\ x^{-\frac{1}{2}}, \ \ \ &x > 0 \end{cases}$$and $[a,b] = [-0.5,1]$. f 