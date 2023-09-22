---
aliases: [vector p-norm, p-norm]
tags: [num]
---
# Vector norm
the p-norm (or vector norm) of a vector x is a measure of its size or magnitude.

#### Definition
![[Pasted image 20230322161729.png]]
$$||x||_p = (|x_1|^p + |x_2|^p + ... + |x_n|^p)^\frac{1}{p}$$
![[Pasted image 20230524140501.png]]
#### Example
- 1-norm (p=1): $\lvert \lvert x \rvert \rvert_{1} = \sum\limits_{i=1}^{n}\lvert x_{i} \rvert$
- 2-norm (Euclidean norm; p=2): $\left( \sum\limits_{i_{1}}^{n}\lvert x_{i} \rvert^{2} \right)^\frac{1}{2}$
- $\infty$-norm (maximum norm, $p=\infty$): $max_{i \in {1,...,n}}\lvert x_{i} \rvert$

## General info
The p-norm generalizes the notion of the absolute value of a number (which is the 1-norm of a scalar) to higher dimensions. It gives us a way to measure the distance between two vectors in n-dimensional space.

When p=2, the p-norm is called the Euclidean norm, and it corresponds to the length of the vector in standard Cartesian coordinates. When p=1, it is called the Manhattan norm or taxicab norm, and it corresponds to the distance between two points in a city grid. When p approaches infinity, it is called the maximum norm or Chebyshev norm, and it corresponds to the maximum absolute value of the components of the vector.

The choice of the p-norm depends on the problem at hand and the specific application. Different norms have different properties, and some may be more appropriate for certain types of data or analysis.