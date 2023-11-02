---
tags: [num]
---
# Forward substitution
start on the left upper corner
![[Pasted image 20230321155150.png]]
Operation count is the same as before ..
**Never** compute the inverse. (more cost i think?)
**Formula**: $$x_{i}= \frac{1}{l_{ii}} \left( b_{i}- \sum\limits_{j=1}^{i-1}l_{ij}x_{j} \right)$$

#### Example
$$\begin{bmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 3 & 4 & 1 \end{bmatrix} \begin{bmatrix} y_{1} \\ y_{2}\\ y_{3} \end{bmatrix} = \begin{bmatrix} 17 \\ 10 \\ -21 \end{bmatrix}$$
$$\begin{align} &y_{1}= 17 \\ &y_{2}= 10-2y_{1}= 10 - 34 = -24 \\ &y_{3}=-21-3y_{1}-4y_{2}= -21-51+96 = 24 \end{align}$$