---
tags: [el]
aliases: [wave equation]
---
# Wave equations

Derived by using the **potential function** (Extending the electic potential ($\vec{E} = - \nabla V$to time-varying fields). 

The wave equation:$$\nabla^{2}V - \mu \varepsilon \frac{\partial^{2} V}{\partial t^{2}} = - \frac{\rho}{\varepsilon}$$which is a scalar non-homogeneous 2nd order differential equation.

The solutions are 
1. Retarded scalar potential: $$V(R,t) = \frac{1}{4 \pi \varepsilon} \int\limits_{V'}^{} \frac{\rho(t-\frac{R}{u})}{R} \ dv' \ \ \ \ [V]$$
2. Retarded vector potential: $$\vec{A}(R,t) = \frac{\mu}{4 \pi}\int\limits_{V'}^{} \frac{\vec{J}(t-\frac{R}{u})}{R} \ dv' \ \ \ \ [Wb/m]$$(This is when substituting $\vec{V}$ with $\vec{A}$). We can then find $\vec{B}$ through $\vec{B}= \nabla \times \vec{A}$.

From lecture:

![[Pasted image 20221130113305.png]]