---
tags: [num]
---
# Perturbation analysis
In numerical analysis, a perturbation refers to a small change or error in the input data of a mathematical problem or algorithm. These small changes can have a significant impact on the output or solution of the problem, leading to numerical instability and inaccuracies. Perturbations can arise from various sources, such as rounding errors in computer arithmetic, measurement errors in scientific experiments, or uncertainties in the initial conditions of a dynamical system. Effective techniques for dealing with perturbations are essential for ensuring the reliability and accuracy of numerical computations in various fields, such as engineering, physics, finance, and computer science.

- Needed for relation between [[backward & forward error]].

Perturbation can occur on the input, the output or …. . A perturbed version of $Ax=b$ is $$ (A+\delta A)\underbrace{ (x+\delta x) }_{ =\tilde x }=(b+\delta b) $$ we assume $A\in\mathbb{R}^{n\times n}$ is invertible, - $\delta A \in\mathbb{R}^{n\times n}$ and $\delta b\in\mathbb{R}^{n}$ are assumed known perturbations in input data (measurement error or rounding error) - $\delta x\in\mathbb{R}^{n}$ is the uncertainty in the solution that we want to estimate.

![[Pasted image 20230322164038.png]]

## Perturbation in b
We start with the analysis for $\lvert \lvert \delta b \rvert \rvert/\lvert \lvert b \rvert \rvert$

- Set $\delta A = 0$, i.e, $$A(x+ \delta x) = (b + \delta b)$$
- Since $Ax = b$ we get $$A \delta x = \delta b \Rightarrow \delta x = A^{-1} \delta b \Rightarrow \lvert \lvert \delta x \rvert \rvert \leq \lvert \lvert A^{-1} \rvert \rvert \ \lvert \lvert \delta b \rvert \rvert$$
- From $Ax = b$ we have $$\lvert \lvert b \rvert \rvert \leq \lvert \lvert A \rvert \rvert \ \lvert \lvert x \rvert \rvert \Rightarrow \lvert \lvert x \rvert \rvert \geq \lvert \lvert b \rvert \rvert / \lvert \lvert A \rvert \rvert$$
- Putting together it gives us $$\frac{\lvert \lvert \delta x \rvert \rvert}{\lvert \lvert x \rvert \rvert} \leq \lvert \lvert A \rvert \rvert \ \lvert \lvert A^{-1} \rvert \rvert \frac{\lvert \lvert \delta b \rvert \rvert}{\lvert \lvert b \rvert \rvert}$$

## Perturbation in A
We repeat the analysis for $\frac{\|\delta A\|}{\|A\|}$ with $\delta b=0$. $$ (A+\delta A)(x+\delta x)=b \Rightarrow Ax+A\delta x+\delta A(x+\delta x)=b $$ since $Ax=b$ we can write $$ \delta x=-A^{-1}\delta A(x+\delta x) \Rightarrow \|\delta x\|\leq\|A^{-1}\|\cdot\|\delta A\|\cdot\|x+\delta x\| $$ dividing by $\|x+\delta x\|$ yields $$ \frac{\|\delta x\|}{\|x\|}\approx \frac{\|\delta x\|}{\|x+\delta x\|}\leq\|A^{-1}\|\cdot\|\delta A\|=\frac{\|A\|\cdot\|A^{-1}\|(\|\delta A\|)}{\|A\|} $$