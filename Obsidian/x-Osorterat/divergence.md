---
tags: [el]
aliases: [divergens, divergent]
---
# Divergence
For [[Gradient]] we considered the spatial derivatives of a [[scalar field]]. Here we consider to the spatial derivatives of a [[vector field]]. This will define both divergence and [[Curl]]

- Used in two of [[Maxwell's equations]]
		- $\nabla \cdot \vec{D} = \rho$ 
		- $\nabla \cdot \vec{B} = 0$
- Divergence of a vector field: $\nabla \cdot \vec{A}$, where $\vec{A}$ is a [[vector field]] in 3D space.


**Definition:**
The divergence of a [[vector field]] $\vec{A}$ at a point is defined as the net outward flux (field lines) of $\vec{A}$ per unit volume as the volume about the point tends to zero. $$div A \overset{\Delta}{=} \lim_{\Delta v\to0} \frac{\oint\limits_{s}^{} \vec{A} \cdot \ d \vec{s}}{\Delta v}$$

## Geometric view
(3b1b)

![[Pasted image 20221216152948.png|500]]

## Proof (definition equals to $\nabla \vec{A}$)
We use [[Cartesian Coordinates]] and choose a point $P(x_{0}, y_{0}, z_{0})$. Geometrically we get a cube with 6 square faces.
For our field $\vec{A}$ at point $P$, the [[Surface integral]] in $div \vec{A}$ can be calculated.
![[Pasted image 20220928103143.png|200]]
Therefore we get $$\oint\limits_{S}^{} \vec{A} \cdot \ d \vec{s} = \text{[sum of all faces integrals] }\vec{A} \cdot d \vec{s}$$
By looking at the front face, assuming $\vec{A}$ constant along it we get $$\begin{flalign}   &\int\limits_{\text{front face}}^{} \vec{A} \cdot \ d \vec{s} = \vec{A}_\text{front face} \cdot \Delta \vec{s}_\text{front face} \\ &= \vec{A}_\text{front} \Delta y \Delta z \vec{a}_{x} =  \\ &= \text{ put in A's and lenghts ...}\end{flalign}$$![[Pasted image 20220928104340.png]]
**And** we then get
![[Pasted image 20220928104209.png]]

For the **back face**, we do a similar procedure, 
![[Pasted image 20220928104620.png]]

**Conclusion:**
The definition of divergence is equal to $\nabla \cdot \vec{A}$.





