---
tags: [el]
---
# Normal component
We find the [[boundary conditions for electrostatic fields|boundary condition]] for this by using [[Gauss law]], for a boundary surface where surface charge of density $\rho_{s}$ exists.
![[Pasted image 20221012105031.png|550]]
Applying the Gaussian surface of small pillbox (top and bottom faces flat) with are of top and bottom faces being $\Delta S$ and height $\Delta h$:
$$LHS=\oint\limits_{S}^{} \vec{D} cd \ d \vec{s} = \left[ \int\limits_{top face}^{} + \int\limits_{bottom face}^{}  + \int\limits_{side face}^{}   \right] \vec{D} \cdot d \vec{s}= \vec{D}_{1} \cdot \vec{a}_{n2} \Delta S 0 \vec{D}_{2} \cdot \vec{a}_{n1}\Delta S$$
[[Gauss law]] states that
$$RHS = \oint\limits_{S}^{} \vec{D} \cdot \ d \vec{s} = Q_{encl} = \rho_{s} \Delta S$$
and noticing $\vec{a}_{n2} = -\vec{a}_{n1}$
By combining these we get $$\begin{flalign}  \vec{a}_{n2} \cdot (\vec{D}_{1} - \vec{D}_{2}) = \rho_{s} \\ D_{1n}- D_{2n} = \rho_{s}\end{flalign}$$
Normal component of electric flux density $\vec{D}$ is **discontinous** across the boundary, with the surface charge denstiy being the magnitude of discontinuity.
**Note:**
1) We derive this using $\vec{D}$ instead of $\vec{E}$ because it's not continous in $\vec{E}_{n}$, because $\varepsilon$ is not the same.
2) When medium 2 is a [[Conductor]] and medium 1 a (linear) [[dielectrics|dielectric]], then: $\vec{D}_{2}=0$ (inside [[Conductor]]) $\Rightarrow D_{2n}=0 \Rightarrow D_{1n} = \rho_{s}= \varepsilon E_{1n}$
3) When both media 1 and 2 are (linear) [[dielectrics]] and $\rho_{s}= 0$: $$D_{1n}=D_{2n} \Leftrightarrow \varepsilon_{1}E_{1n} = \varepsilon_{2}E_{2n}$$
4) Concept of [[Gauss law]] useful even here! The behaviour of scalar [[electric potential]] $V$. $V$ is **continous** across boundary because $$\Delta V = - \int\limits_{C}^{} \vec{E} \cdot \ d \vec{l}=0$$ but $\Delta V = V(\vec{b})-V(\vec{a}) = 0$  since $\Delta V = 0$ and $V(\vec{b}) = V(\vec{a})$