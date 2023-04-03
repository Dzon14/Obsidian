---
tags: [num]
---
# Newton interpolation
- A form of [[polynomial interpolation]]
- Uses [[divided differences]] in calculation (of system matrix?)

$$\phi_{i}(x) = \prod\limits_{k=0}^{i-1}(x-x_{k}), \ \ \ i=0,1,...,n$$
![[Pasted image 20230328145431.png]]
- $x_{0}, ..., x_{N-1}$ are called the *centers* of the Newton polynomial
-  [uses [[nested multiplication|Horners method]]
- System matrix:  alower [[triangular matrix]]: $$\begin{bmatrix}
1 & 0 & 0 & 0 & 0 \\
1 & \phi_1(x_1) & 0 & 0 & 0 \\
1 & \phi_1(x_2) & \phi_2(x_2) & 0 & 0 \\
1 & \phi_1(x_3) & \phi_2(x_3) & \phi_3(x_3) & 0 \\
1 & \phi_1(x_4) & \phi_2(x_4) & \phi_3(x_4) & \phi_4(x_4)
\end{bmatrix}
\begin{bmatrix}
c_0 \\
c_1 \\
c_2 \\
c_3 \\
c_4
\end{bmatrix}
=
\begin{bmatrix}
f_0 \\
f_1 \\
f_2 \\
f_3 \\
f_4
\end{bmatrix}$$which require $2n^{2}$ FLOPs. 

## Advantage with Newton basis functions
- compared to monomial basis functions, this is comparatively vheap to add a new data point at a late stage of the computations.  The system matrix does not need to be solved again, we can just add a new bottom row.


