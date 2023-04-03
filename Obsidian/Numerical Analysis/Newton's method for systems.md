---
tags: [num]
---
# Newton's Method for Systems
- Finds root of a system of [[nonlinear equation|nonlinear equations]].
- Updating an initial estimate of the solution usin [[Jacobian matrix]].

## Formula
See the standard formula as if it contains vectors. When derivating we get $\bar{f}(\bar{x}_{n}) + J_{\bar{f}}(\bar{x}_{n})d \bar{x}_{n}= \bar{0}$, here J is the [[Jacobian matrix]].

The iteration formula becomes $$\begin{align} d \bar{x}_{n}= - J_{\bar{f}}(\bar{x}_{n})^{-1} \bar{f}(\bar{x}_{n}) \\ \bar{x}_{n+1} = \bar{x}_{n}+d \bar{x}_{n} \end{align}$$
## Numerical example
![[Pasted image 20230403174232.png|550]]

## Example
![[Pasted image 20230403174446.png|500]]
![[Pasted image 20230403174504.png|500]]
