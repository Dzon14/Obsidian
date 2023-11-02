---
tags: [num]
---
# Jacobi method

- The simplest [[fixed-point iterative methods]]
- Look in the end of this document for a good example for when it works and when it doesn't.

## Separation
Start with $Ax = b$ and,
Separate A as $$A = L + D + U$$where 
- $D = diag(A)$ 
- $L = \text{ lower triangular part (below diagonal) of A}$
- $U = \text{ upper triangular part (above diagonal) of A}$
![[Pasted image 20230327154552.png]]
we now get $$Ax = b \Leftrightarrow (L+D+U)x =b$$which can be rewritten to $$\begin{align} D&x = - (L+U)x+b \\ &x= -D^{-1}(L+U)x+D^{-1}b \end{align}$$comparing this to $x=Bx+c$ , Jacobi gives us $$B=-D^{-1}(L+U) \ \ \text{ and } \ \ c=D^{-1}b$$
## Method - computational view
Set $P = D$ and $N = P-A = -(L+U)$ then we get (using [[splitting]] method): $x_{k+1} = P^{-1}Nx_{k}+P^{-1}b$
we get the *Jacobi method*: $$x_{k+1}= \underbrace{-D^{-1}(L+U)x_{k}}_{B} + \underbrace{D^{-1}b}_{c}$$
- This iteration needs the trivial inversion of the diagonal matrix D, i.e $Dx_{k}= y$ is very easy to solve...?
- A $\sim$ D if A is a [[strictly diagonally dominant matrix]]

- **Theroem:** If $A \in \mathbb{R}^{nxn}$ is strictly diagonally dominant, then for every vector $b \in \mathbb{R}^{n}$ and every starting guess $x_{0} \in \mathbb{R}^{n}$ the Jacobi method applied to $Ax = b$ converges to a solution of it. 
Proof: $$A = \begin{bmatrix} 10 & 1 & 2 \\ -1 & -5 & 3 \\ 2  & 3 & 7  \end{bmatrix} \sim D= \begin{bmatrix} 10 & 0  & 0 \\ 0 & -5 & 0 \\ 0 & 0  & 7 \end{bmatrix}$$
![[Pasted image 20230327155824.png|500]]

## Example
![[Pasted image 20230327160205.png|500]]
![[Pasted image 20230327160216.png|500]]

## Example from book
![[Pasted image 20230330105318.png]]
**NOTE:** If we get the equations in the the reverse order: $u+2v =5, \ 3u+v = 5$ we will get a different u and v which will lead to the iterations diverging instead of [[convergence|converging]]. In other words, the Jacobi method *fails*. To know this condition we'll use [[strictly diagonally dominant matrix]]. We get this from the following theorem:
##### Theorem 2.10
If the $n \times n$ matrix A is strictly diagonally dominant, then (1) A is a nonsingular matrix, and (2) for every vector b and every starting guess, the Jacobi Method applied to $Ax = b$ *converges* to the (unique) solution.

Furthermore, if we want to it as a **separation**, the system of equations Ax = b can be rearranged in a fixed-point iteration of form: $$\begin{align} Ax = b \Leftrightarrow x=D^{-1}(b-(L+U)x) \end{align}$$ **Note**: Since D is a diagonal matrix, its inverse is the matrix of reciprocals of the diagonal entries of A. The Jacobi Method is just the fixed-point iteration of equation above: $$x_{k+1}=D^{-1}(b-(L+U)x_{k})$$for $k=0,1,2,...$ and $x_{0}=\text{ initial vector}$. So for the same example as above we get: ![[Pasted image 20230330111220.png]]