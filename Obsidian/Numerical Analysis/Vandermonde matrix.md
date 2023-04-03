---
tags: [num]
---
# Vandermonde matrix
The Vandermonde matrix is a square matrix with the terms of a geometric progression as its elements. Specifically, given a vector of distinct numbers x = $x_1, x_2, ..., x_n$, the Vandermonde matrix V with n rows and n columns is defined as:

$V = x^0, x^1, x^2, ..., x^{(n-1)}$,

where $x^k$ denotes the kth power of x and the superscripts denote element-wise exponentiation.

The Vandermonde matrix is commonly used in polynomial interpolation, where given a set of n points $(x_1, y_1), (x_2, y_2), ..., (x_n, y_n)$, one seeks a polynomial of degree at most n-1 that passes through all the points. The Vandermonde matrix is used to set up and solve the resulting linear system of equations.

## Example 
$$ P_n(x)=\sum\limits_{i=0}^{n}c_ix^{i} $$ and the system becomes $$ \begin{pmatrix} 1 & x_0 & x_0^2 & x_0^3 & x_0^4 \\ 1 & x_1 & x_1^2 & x_1^3 & x_1^4 \\ 1 & x_2 & x_2^2 & x_2^3 & x_2^4 \\ 1 & x_3 & x_3^2 & x_3^3 & x_3^4 \\ 1 & x_4 & x_4^2 & x_4^3 & x_4^4 \\ \end{pmatrix} \begin{pmatrix} c_0 \\ c_1 \\ c_2 \\ c_3 \\ c_4 \\ \end{pmatrix} = \begin{pmatrix} f_0 \\ f_1 \\ f_2 \\ f_3 \\ f_4 \\ \end{pmatrix} $$