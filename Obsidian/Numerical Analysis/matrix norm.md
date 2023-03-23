---
tags: [num]
---
# Matrix norm

The matrix norm on $\mathbb{R}^{nxn}$ induced by the vector p-norm is defined as $$\lvert \lvert A \rvert \rvert_{p} := \underset{x \in \mathbb{R}^{n}/\{0\}}{sup} \frac{\lvert \lvert Ax \rvert \rvert_{p}}{\lvert \lvert x \rvert \rvert_{p}}, \ \ 1 \leq p \leq \infty$$for $A \in \mathbb{R}^{nxn}$
![[Pasted image 20230322162342.png]]
- see [[supremum]]

**Remark:**$$\begin{align} &1. \lvert \lvert A \rvert \rvert_{1} = max_{1\leq j \leq n} \sum\limits_{i=1 }^{n}\lvert a_{ij}  \rvert \\ &2. \lvert \lvert A \rvert \rvert_{\infty} max_{1 \leq i \leq n}\sum\limits_{j=1 }^{n} \lvert  a_{ij} \rvert \end{align}$$Max av summan av kolonner (1) eller rader (2)
*Example:*
Let $$A = \begin{bmatrix} 2 & 4 \\ 2 & 1 \end{bmatrix}$$
- $\lvert \lvert A \rvert \rvert_{1} = 5$
- $\lvert \lvert A \rvert \rvert_{\infty}= 6$
![[Pasted image 20230322163443.png]]
