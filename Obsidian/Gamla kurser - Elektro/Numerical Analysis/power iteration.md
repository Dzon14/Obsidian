---
tags: [num]
---
# Power iteration
- The motivation behind Power Iteration is that multiplication by a matrix tends to move vectors toward the dominant eigenvector direction.
- An iterative method used to find the dominant eigenvalue and its corresponding eigenvector of a given matrix. It is primarily used for estimating the largest eigenvalue in terms of magnitude, often referred to as the spectral radius.
- The power iteration algorithm starts with an initial vector and iteratively applies the matrix to the vector, normalizing it at each step. As the iterations progress, the vector converges to the eigenvector corresponding to the dominant eigenvalue. The dominant eigenvalue can then be estimated by taking the ratio of successive vector components.

## Rayleigh quotient
$$\lambda = \frac{x^{T}Ax}{x^{T}x}=x^{T}Ax$$

## Power iteration

![[Pasted image 20230516142133.png|550]]
![[Pasted image 20230516142347.png|550]]

## Definition - dominant eigenvalue
Let A be an $m × m$ matrix.Adominant eigenvalue of A is an eigenvalue λ whose magnitude is greater than all other eigenvalues of A. If it exists, an eigenvector associated to λ is called a dominant eigenvector.

## Formula from book
![[Pasted image 20230516142707.png]]
