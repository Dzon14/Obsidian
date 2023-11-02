---
tags: [num]
---
# Least Squares 
- A method for approximating solutions to an over-determined system of equations. It is used when there are more equations than unknowns, so there is no exact solution. The goal of the least squares method is to find a solution that minimizes the sum of the squares of the residuals, which are the differences between the predicted values and the actual values.
- The method involves constructing a matrix equation of the form Ax=b, where A is an m x n matrix with m > n, x is an n x 1 column vector of unknowns, and b is an m x 1 column vector of known values. The least squares solution is obtained by minimizing the squared norm of the residual vector, which is defined as r = b - Ax.
- There are several algorithms for computing the least squares solution, including the normal equations method, QR decomposition, and singular value decomposition.

## [[least square approximation]]

## Finding the least squares solution
For a general overdetermined linear system $Ax=b$ the least squared solution $x \in \mathbb{R}^{n}$ can be obtained by solving the **normal equations** $$A^{T}Ax= A^{T}b$$$A^TA$ has dimensions $n \times n$ and $A^{T}b$ is a column vector with n entries so the whole equation is a $n \times n$ linear system for x.
The **normal equations** can be derived 

#### Normal equations for least squares
Given $Ax = b$ solve $$A^{T}A \vec{x} = A^{T}b$$for the least squares solution $\vec{x}$ that minimizes the Euclidean length of the residual $r = b-Ax$.

## Computing the least squares solution (MATLAB)
$$x = A \backslash b$$
![[Pasted image 20230424160337.png]]
![[Pasted image 20230424160353.png]]

#### Example from book 
4.1: 
![[Pasted image 20230424162604.png]]
![[Pasted image 20230424162628.png]]

## Squared error (SE) and root mean squared error (RMSE)
![[Pasted image 20230424162802.png]]

#### Example from book on RMSE
![[Pasted image 20230424162840.png]]

## Fitting models to data
![[Pasted image 20230424162953.png]]
![[Pasted image 20230424163005.png]]
4.2:
![[Pasted image 20230424163141.png]]
which is from 4.1