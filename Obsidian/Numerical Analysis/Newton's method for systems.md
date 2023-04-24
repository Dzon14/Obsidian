---
tags: [num]
aliases: [multivariate Newtons method]
---
# Newton's Method for Systems
- Finds root of a system of [[nonlinear equation|nonlinear equations]].
- Updating an initial estimate of the solution using [[Jacobian matrix]].

## Formula
See the standard formula as if it contains vectors. When derivating we get $\bar{f}(\bar{x}_{n}) + J_{\bar{f}}(\bar{x}_{n})d \bar{x}_{n}= \bar{0}$, here J is the [[Jacobian matrix]].

The iteration formula becomes $$\begin{align} d \bar{x}_{n}= - J_{\bar{f}}(\bar{x}_{n})^{-1} \bar{f}(\bar{x}_{n}) \\ \bar{x}_{n+1} = \bar{x}_{n}+d \bar{x}_{n} \end{align}$$or in the book $$x_{k+1}=x_{k}- (DF(x_{k}))^{-1}F(x_{k})$$where we also have a initial vector $x_{0}$ and DF is the [[Jacobian matrix]]. The iteration step for multivariate [[Newton's method]] is $$\begin{cases} \begin{align} &DF(x_{k})s = -F(x_{k}) \\ &x_{k+1} = x_{k}+s \end{align} \end{cases}$$

## Numerical example
![[Pasted image 20230403174232.png|550]]

## Example
![[Pasted image 20230403174446.png|500]]
![[Pasted image 20230403174504.png|500]]

## Example from book
![[Pasted image 20230421140201.png|600]]
![[Pasted image 20230421140238.png|600]]

