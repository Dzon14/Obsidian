---
aliases: [LU, LU factorisation]
tags: [num]
---
# LU factorization
A matrix $A \in \mathbb{R}^{nxn}$ has a LU decomposition if it can be expressed as the product$$A=LU$$where L is a lower [[triangular matrix]] and U is an upper [[triangular matrix]].
E.g.
$$A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ l_{21} & 1 & 0 \\ l_{32} & l_{32} & 1 \end{bmatrix} \cdot \begin{bmatrix} u_{11} & u_{12} & u_{13} \\ 0 & u_{22} & u_{23} \\ 0 & 0 & u_{33} \end{bmatrix}$$
## How to solve $Ax = b$ via LU decomposition
If we have L and U such that $A = LU$  $$ \Rightarrow LUx = b$$where $Ux =: y$
1. Solve triangular system $Ly = b$ ([[forward substitution]]) $\rightarrow$ y
2. Solve triangular system $Ux = y$ ([[back substitution]]) $\rightarrow x$
The LU factorization is a matrix representation of [[Gauss elimination|Gauss elimination]].
To get the LU of matrix A:

consider the case $n=3$ 
$$A = \begin{bmatrix} a & b & g \\ c & d & h \\ e & f & i \end{bmatrix} \in \mathbb{R}^{3x3}$$ Multiply it with the identity matrix from the left. 
Step 1:
![[Pasted image 20230321163949.png]]
Step 2: New pivot is $d-\frac{c}{a}b$ and do analogously as before
![[Pasted image 20230321164004.png]]
The left matrix becomse L and the right U.

## Computational complexity of LU factorization
$$\frac{2}{3}n^{3}- \frac{1}{2}n^{2}- \frac{1}{6}n$$

## LU decomposition with [[pivoting]]
- if pivot is 0 we cannot do LU decomposition since we don't do interchange?
- See [[permutation matrices|permutation matrix]]

If A is nonsingular, there is a P such that $PA = LU$ $$Ax = b \Rightarrow LUx = Pb$$
1. Compute L, U and P
2. Compute Pb
3. Solve Ly = Pb with [[forward substitution]]
4. Solve Ux = y with [[back substitution]]

#### Example
$$A = \begin{bmatrix} 2 & 1 & 5 \\ 4 & 4 & -4 \\ 1 & 3 & 1 \end{bmatrix}, \ b = \begin{bmatrix} 5 \\ 0 \\ 6 \end{bmatrix}$$
Step 1: $$\begin{bmatrix} 2 & 1 & 5 \\ 4 & 4 & -4 \\ 1 & 3 & 1 \end{bmatrix} , \ P = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix} \Rightarrow \begin{bmatrix} 4 & 4 & -4 \\ 2 & 1 & 5 \\ 1 & 3 & 1 \end{bmatrix} $$(switch row 1 and 2 because 2 has the largest element in [[pivoting|pivot]]). We also take $\frac{1}{2}$ times row 1 and subtracts it from 2. The $\frac{1}{2}$ that is put into the first column of row 2 is actually a part of the L-matrix. 

$$\Rightarrow \begin{bmatrix} 4 & 4 & -4 \\ \frac{1}{2} & -1 & 7 \\ \frac{1}{4} & 2 & 2\end{bmatrix} , \ \begin{bmatrix} 0 & 1 & 0 \\ 0  & 0 & 1 \\ 1 & 0 & 0\end{bmatrix}\Rightarrow \begin{bmatrix} 4 & 4 & -4 \\ \frac{1}{4} & 2 & 2 \\ \frac{1}{2} & -1 & 7 \end{bmatrix}$$(we switch the last two rows) $$\Rightarrow \begin{bmatrix} 4 & 4 & -4 \\ \frac{1}{4} & 2 & 2 \\ \frac{1}{2} & -\frac{1}{2} & 8 \end{bmatrix}$$We now get LU: $$L \cdot U = \begin{bmatrix} 1 & 0 & 0 \\ \frac{1}{4} & 1 & 0 \\ \frac{1}{2} & -\frac{1}{2} & 1 \end{bmatrix} \cdot \begin{bmatrix} 4 & 4 & -4 \\ 0 & 2 & 2 \\ 0 & 0 & 8 \end{bmatrix} = \begin{bmatrix} 4 & 4 & -4 \\ 1 & 3 & 1 \\ 2 & 1 & 5 \end{bmatrix} = P \cdot A$$

