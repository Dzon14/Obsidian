---
tags: [el]
---
# Boundary Conditions for static magnetic fields
(In vacuum we cannot have a boundary condition)

## Three tasks

### Task 1 - Normal component
We can motivate in the same way as for [[boundary conditions for electrostatic fields]].
Resulting in that for the normal component of $\vec{D}$, we get $\vec{a}_{n2} \cdot (\vec{D}_{1}-\vec{D}_{2}) = \rho_{s}$ or $D_{1n}-D_{2n}= \rho_{s}$.
$\nabla \cdot \vec{D}=\rho$
We use the result directly for the $\vec{B}$ field by first noticing that $\oint\limits_{S}^{} \vec{B } \cdot \ d \vec{s} = \int\limits_{V}^{} \nabla \cdot \vec{B} \ dv$ ([[Divergence theorem]]). 
we know that $\nabla \cdot \vec{B}=0$, so $\oint\limits_{S}^{} \vec{B} \cdot \ d \vec{s}=0$. 
Replacing $\vec{D}$ with $\vec{B}$ and set $\rho_{s}=0$ in $\vec{a}_{n2} \cdot (\vec{D}_{1}-\vec{D}_{2})= \rho_{s}$: $$\begin{align} &\vec{a}_{n2} \cdot (\vec{B}_{1}-\vec{B}_{2})=0 \\ &B_{1n}=B_{2n} \end{align}$$(for linear magnetic materials).
$\Rightarrow$ Normal component of the $\vec{B}$ field is **continous** across a boundary
**Note:**
1) For linear magnetic materials $B_{1n}=B_{2n} \Leftrightarrow \mu_{1}H_{1n}=\mu_{2}H_{2n}$
2) We can go through the same derivation as for $\vec{D}$ to find boundary condition for the normal component of $\vec{B}$, byt why not use existin result!

### Task 2 - Tangential component
(See lecture for derivation)

We can follow a similar approach as in finding it for the electric field, however now $\oint\limits_{C}^{} \vec{E} \cdot \ d \vec{l}=0$
- See lecture for derivation and proof

We get $$\begin{align} \Rightarrow H_{1t} - H_{2t} = J_{sn} \ \ [A/m] \ \ \text{ or } \\ \vec{a}_{n2} \times (\vec{H}_{1}-\vec{H}_{2})=\vec{J}_{s} \ \ [A/m] \end{align}$$
$\Rightarrow$ Tangential component of $\vec{H}$ is **discontinous** across the boundary by the amount $J_{sn}$ where a free surface current exists.
However if conductivity $\sigma$ is finite (exception for superconductor), then there can be only volume current densities in the media and $J_{sn}=0 \Rightarrow H_{1t}= H_{2t}$
$\Rightarrow$ Tangential component is then **continous** across the boundary in most materials-
- linear magnetic materials $\frac{B_{1t}}{\mu_{1}}=\frac{B_{2t}}{\mu_{2}}$

### Task 3
![[Pasted image 20221121105411.png]]

Conclusion: $$\Phi_{m} = 0 \ \ \text{ no flux passing through } \rightarrow A_{1t}=A_{2t} \ \ (continous)$$.

