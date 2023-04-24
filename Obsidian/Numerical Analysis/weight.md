---
aliases: [weights]
tags: [num]
---
# Weight
The coefficients used to compute a weighted sum or integral approximation. weights are used in quadrature rules (such as [[Gaussian quadrature]]) to determine the contribution of each function evaluation at specific nodes to the overall approximation. The weights are usually chosen to optimize the accuracy of the approximation based on the properties of the integrand and the quadrature rule being used.

$$w_{i} = \int\limits_{a}^{b} \phi_{i}(x) \ dx = \int\limits_{a}^{b} L_{i}^{N}(x) \ dx$$
- Quadrature rules derived with Lagrange using equidistant nodes are called [[Newton-Cotes quadrature]] rules.
		- Useful for ex. when integratind data measured at regularly recurring times. 
- [[Gaussian quadrature]] uses non-equidistant spacing for the nodes, which is more efficient if the circumstances permit such spacing.