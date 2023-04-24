---
tags: [num]
aliases: [the method of least squares]
---
# Least Square Approximation 
- Least squares approximation, on the other hand, is a specific application of the least squares method, where we are trying to approximate a given function by a simpler function, such as a polynomial. The goal is to find the coefficients of the simpler function that minimize the sum of the squares of the differences between the given function and the approximation at a set of discrete points.
- We want to fit a simple function to a large set of measured data points, possibly affected by measurement error (noise). The aim is not to [[interpolation|interpolate]] the data, but rather to capture general trends
- The solution for x is the least square solution

If we have three data point which makes up a linear function $f(x) = c_{0}+c_{1}x$ and then try to use polynomial interpolation, we will end up with a **overdetermined** linear system $$\begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix} \begin{bmatrix} c_{0} \\ c_{1} \end{bmatrix} = \begin{bmatrix}  1 \\ 2 \\ 2 \end{bmatrix}$$(Ac = b). Meaning, therer are more equations than unknown and it has no solution $c$ which makes $Ac=b$. The *idea* is to not solve the linear system exactly but to find the "least bad solution" c that minimizes the norm of the residual vector $$r \equiv b- Ac$$
If by chance c was a solution to the linear system we would have $\lvert \lvert r \rvert \rvert = 0$, but that is unlikely to happen. We instead seek the $c = [c_{0};c_{1}]$ which minimizes $\lvert \lvert r \rvert \rvert$. This gives us the linear function $f(x) = c_{0}+ c_{1}x$ which is the best approximation to the data. In our example (overdetermined linear system), the three entries of residual are $$r = \begin{bmatrix} [r_{0} \\ r_{1} \\ r_{2} \end{bmatrix} = \begin{bmatrix} 1-c_{0}-c_{1} \\ 2-c_{0}- 2c_{1} \\ 2- c_{0}- 3c_{1} \end{bmatrix}$$ and we now seek the $c$ that minimizes the $\infty$-norm of r $$\lvert \lvert r \rvert \rvert_{\infty} = max(\lvert r_{0} \rvert, \lvert r_{2} \rvert) = max(\lvert 1-c_{0}-c_{1} \rvert, \lvert 2-c_{0}-2c_{1} \rvert, \lvert 2-c_{0}-3c_{1} \rvert).$$Finding this c is generally hard (a minimax problem). However, in this example we can show that the minimum is attained when $\lvert r_{0} \rvert = \lvert r_{1} \rvert = \lvert r_{2} \rvert$ and that $(c_{0},c_{1}) = \left( \frac{3}{4}, \frac{1}{2} \right)$ produces that minimum.

Let us then seek the c that minimizes the **2-norm** of $r$. $$\lvert \lvert r \rvert \rvert_{2} = ((1-c_{0}-c_{1})^{2} + (2-c_{0}-2c_{1})^{2} + (2-c_{0}-3c_{1})^{2})^{\frac{1}{2}}$$By taking partial derivatives of $\lvert \lvert r \rvert \rvert_{2}$ with respect to $c_{0}$ and $c_{1}$ and setting these to zero, we can find the stationary point $(c_{0},c_{1}) = (2/3, 1/2)$, which is a minimum. Because of the squared expression in equation above, this minimizer is called *least squares solution* to the overdetermined system in the beginning.
- The least square solution to an overdetermined linear system is easier to compute than other solutions, obtained by minimizing $\lvert \lvert r \rvert \rvert_{p}$ for $p \neq 2$.
- Approximating sets of data points by combinations of simple functions with coefficients from least squares solutions to overdetermined systems is often, somewhat imprecisely, called *least squares approximation* or *the method of least squares*