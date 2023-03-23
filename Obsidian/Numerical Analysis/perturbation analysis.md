---
tags: [num]
---
# Perturbation analysis
![[Pasted image 20230322164038.png]]

## Perturbation in b
We start with the analysis for $\lvert \lvert \delta b \rvert \rvert/\lvert \lvert b \rvert \rvert$

- Set $\delta A = 0$, i.e, $$A(x+ \delta x) = (b + \delta b)$$
- Since $Ax = b$ we get $$A \delta x = \delta b \Rightarrow \delta x = A^{-1} \delta b \Rightarrow \lvert \lvert \delta x \rvert \rvert \leq \lvert \lvert A^{-1} \rvert \rvert \ \lvert \lvert \delta b \rvert \rvert$$
- From $Ax = b$ we have $$\lvert \lvert b \rvert \rvert \leq \lvert \lvert A \rvert \rvert \ \lvert \lvert x \rvert \rvert \Rightarrow \lvert \lvert x \rvert \rvert \geq \lvert \lvert b \rvert \rvert / \lvert \lvert A \rvert \rvert$$
- Putting together it gives us $$\frac{\lvert \lvert \delta x \rvert \rvert}{\lvert \lvert x \rvert \rvert} \leq \lvert \lvert A \rvert \rvert \ \lvert \lvert A^{-1} \rvert \rvert \frac{\lvert \lvert \delta b \rvert \rvert}{\lvert \lvert b \rvert \rvert}$$

## Perturbation in A
![[Pasted image 20230322164721.png]]
