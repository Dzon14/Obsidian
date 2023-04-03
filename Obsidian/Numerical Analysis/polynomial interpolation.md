---
tags: [num]
---
# Polynomial interpolation
![[Pasted image 20230327163132.png|500]]
**Polynomial space:**
![[Pasted image 20230327164114.png]]
**Task:**
Let $(x_{n}, f_{n})^{N}_{n=0}$ a set of pairs of numbers. Determine a suitable polynomial $P_{N}\in \mathbb{P}_{N}$ with $$P_N (x_{n}) = f_{n} \ \ \ \ n=0,...,N$$
Polynomial interpolation means that one seeks a single polynomial $P_{n}(x)$ of degree $n$ that fits all the $n+1$ data points of $$(x_{i}f_{i}), \ \ i=0,1,...,n$$This polynomial is unique and often written in the form $$P_n(x) = \sum\limits_{i=0}^{n}c_{i}\phi_{i}(x)$$where $c_{i}$ are coefficients and $\phi_{i}(x)$ are *basis functions*. The $n+1$ coefficients $c_{i}$ are found by enforcing that the $n+1$ equation is given by $$P(x_{i}) = f_{i}, \ \ \ i =0,1,...,n$$This gives a linear system for the $c_{i}$:s which, for the case $n=4$ has the form $$\begin{bmatrix} \phi_0(x_0) & \phi_1(x_0) & \phi_2(x_0) & \phi_3(x_0) & \phi_4(x_0) \\ \phi_0(x_1) & \phi_1(x_1) & \phi_2(x_1) & \phi_3(x_1) & \phi_4(x_1) \\ \phi_0(x_2) & \phi_1(x_2) & \phi_2(x_2) & \phi_3(x_2) & \phi_4(x_2) \\ \phi_0(x_3) & \phi_1(x_3) & \phi_2(x_3) & \phi_3(x_3) & \phi_4(x_3) \\ \phi_0(x_4) & \phi_1(x_4) & \phi_2(x_4) & \phi_3(x_4) & \phi_4(x_4) \\ \end{bmatrix} \begin{bmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \\ \end{bmatrix} = \begin{bmatrix} f_0 \\ f_1 \\ f_2 \\ f_3 \\ f_4 \\ \end{bmatrix}$$Common choices for the $\phi_{i}(x)$ are **monomial base functions, Lagrange basis functions** and **Newton basis functions**. When determing which set of basis functions is best suited in a situation we must consider:
- The cost of obtaining the $c_{i}$ 
- The cost of evaluating the $\phi_{i}(x)$
- The accuracy requested
No set of basis functions is the best in all situations. 

## Polynomial interpolation with *monomial basis functions*
- $\phi_{i}(x) = x^{i}$. The interpolating polynomial becomes $$P_{n}(x) = \sum\limits_{i=0}^{n}c_{i}x^{i}$$ and the system becomes $$ \begin{bmatrix} 1 & x_0 & x_0^2 & x_0^3 & x_0^4 \\ 1 & x_1 & x_1^2 & x_1^3 & x_1^4 \\ 1 & x_2 & x_2^2 & x_2^3 & x_2^4 \\ 1 & x_3 & x_3^2 & x_3^3 & x_3^4 \\ 1 & x_4 & x_4^2 & x_4^3 & x_4^4 \\ \end{bmatrix} \begin{bmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \\ \end{bmatrix} = \begin{bmatrix} f_0 \\ f_1 \\ f_2 \\ f_3 \\ f_4 \\ \end{bmatrix} $$This sysmte matrix is called a [[Vandermonde matrix]]. 

## Polynomial interpolation with Lagrange basis functions
- [[Lagrange interpolation]]

## Polynomial interpolation with Newton basis functions
- [[Newton interpolation]]
- Uses [[divided differences]]