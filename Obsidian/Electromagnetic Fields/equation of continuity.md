---
tags: [el]
---
# Equation of Continuity
Using conservation of charges (electric charges cannot be created or destroyed).
- If volume V contains total charge Q, net current out of $S \Leftrightarrow \text{total charge Q must decrease}$
- We know $I = \oint\limits_{S}^{} \vec{J} \cdot \ d \vec{s} = - \frac{dQ}{dt}$
![[Pasted image 20221107102538.png|250]]
By rewriting Q and then applying [[Divergence theorem]], we get $$\nabla \cdot \vec{J} = - \frac{\partial \rho}{\partial t} \ \ \ [Am^{-3}]$$
which is the equation of continuity in **point form**.

Since steady electric current, $$\frac{\partial \rho}{\partial t} = 0 \Rightarrow \nabla \cdot \vec{J} = 0$$
which is a divergenceless [[vector field]]. This means the field lines of $\vec{J}$ always close in on themselves.
By [[Divergence theorem]] $\oint\limits_{S}^{} \vec{J} \cdot \ d \vec{s} = \int\limits_{V}^{} \nabla \cdot \vec{J} \ dv = 0$.

For n interconnected conducting wires $$\oint\limits_{S}^{}  \vec{J} \cdot \ d \vec{s} \Rightarrow \sum\limits_{j=1}^{n}I_{j} = 0$$which is [[Kirchhoff's current law]], which states that the algebraic sum of all currents flowing out of a junction in an electric circuit is zero.
![[Pasted image 20221107104042.png|300]]
Where all currents (integral of each $\vec{J}$) is 0.