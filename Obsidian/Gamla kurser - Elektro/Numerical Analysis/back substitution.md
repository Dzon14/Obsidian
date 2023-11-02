---
tags: [num]
---
# Back substitution
start on the right lower corner
![[Pasted image 20230321154153.png]]
**Formula:**
$$x_{i}= \frac{1}{u_{ii}} \left( b_{i}-\sum\limits_{j=i+1}^{n}u_{ij}x_{j}  \right)$$
FLOPs : $n^{2}$
#### Example
$$\begin{bmatrix} 1 & 2 & 3 \\ 0 & 4 & 5 \\ 0 & 0 & 6 \end{bmatrix} \begin{bmatrix} x_{1} \\ x_{2}\\ x_{3} \end{bmatrix}= \begin{bmatrix} 7 \\ 8\\ 9 \end{bmatrix}$$
We get $$\begin{align} &x_{3}= \frac{9}{6} \\ &x_{2}= (8-5x_{3}) \frac{1}{4} \\ &x_{1}= (7-(3x_{3}+2x_{2}))\frac{1}{1}\end{align}$$