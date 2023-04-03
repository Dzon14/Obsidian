---
tags: [num]
aliases: [backward error, forward error]
---
# Backward/Forward error

![[Pasted image 20230322163629.png]]
- Both backward error and forward error has $\lvert \lvert  \rvert \rvert_\infty$ (also for the relative errors)
- There exists a general relationship between relative forward error and relative backward error.
- $\tilde{x} = x_{a}$

**Residual:** In mathematics, residual refers to the difference between the actual value of a dependent variable and the predicted value of that variable based on a given model or equation.

**Forward error**:
imagine input $\rightarrow$ output (through a "box")

## Relation between forward and backward error
For this relation we need [[perturbation analysis]]

## Error magnification factor
$$\text{error magnification factor } = \frac{\text{relative forward error}}{\text{relative backward error}} = \frac{\frac{\lvert \lvert x - x_{a} \rvert \rvert_\infty}{\lvert \lvert x \rvert \rvert_\infty}}{\frac{\lvert \lvert r \rvert \rvert_\infty}{\lvert \lvert b \rvert \rvert_\infty}}$$
The [[condition number]] of a square matrix A, $cond(A) = \mathcal{k}_{p}(A)$, is the maximum possible error magnification factor for solving Ax = b, over all right-hand sides b
