---
tags: [el]
---
# Vector Magnetic Potential 
From Biot-Savart Law, we can calculate that $\nabla \cdot \vec{B}=0$ (net outward flux is zero) In [[Elmagi F5]], it was shown using one of two [[Null identities]] that if a [[vector field]] is divergenceless (i.e., solenoidal field, with field lines closing in on themselves), then it can be expressed as the [[Curl]] of another [[vector field]] , i.e. $\vec{B}= \nabla \times \vec{A}$, where $\vec{A}$ is the **vector magnetic potential**. How does this compare with the definition of [[Electric potential]] in [[Electrostatics]]?

To define the vector $\vec{A}$, we need to specify its [[divergence]] and [[Curl]]. $\nabla \cdot \vec{A}$ can be specified to simplify calculation of $\vec{A}$.

- We can **derive** $\vec{A}$ from [[Ampere's circuital law]] in point form.

In the derivation we find the vector [[Poisson's equation]]: $$\nabla^{2} \vec{A} = - \mu_{0}\vec{J}$$with the solution to Possion being: $$\begin{align}  &\vec{A} = \frac{\mu_{0}}{4 \pi} \int\limits_{V'}^{} \frac{\vec{J}}{R} \ dv' \ \ [Wb/m] \\ &\text{or equivalently for thin wire}, \\ &\vec{A}=\frac{\mu_{0}I}{4 \pi}\oint\limits_{C'}^{} \frac{d \vec{l}'}{R} \end{align}$$
See: [[magnetic flux]] and its relation to $\vec{A}$.
Physical interpretation: Circulation of A around C equals the total magnetic flux passing through the surface enclosed by the flux.

- We also have $$\vec{B} = \nabla \times \vec{A}$$

## Exempel
![[Pasted image 20221114115606.png]]
![[Pasted image 20221114115620.png]]
![[Pasted image 20221114115655.png]]
(m is the [[magnetic dipole moment]])

**Note:**
The current-carrying loop is called a magnetic dipole, which can be compared to the [[electric dipole]] in [[Electrostatics]].