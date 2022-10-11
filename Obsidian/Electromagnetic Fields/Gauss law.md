---
tags: [el]
---
# Gauss law
Using [[Divergence theorem]] we can write the integral form
$$\nabla \cdot \vec{D} = \rho \Rightarrow \int\limits_{V}^{} \nabla \cdot \vec{D} \ dv = \oint\limits_{s}^{} \vec{D} \ d \vec{s} = \int\limits_{V}^{} \rho \ dv \Rightarrow \oint\limits_{S}^{} \vec{D} \cdot \ d \vec{s} = Q$$
- $\vec{D}$ is the electric flux density. $\vec{D} = \varepsilon_{0}\vec{E}$
- $Q$ is the total charge enclose by $V$ or $S$.

To derive Gauss Law, take the [[divergence]] of the [[Electric field]], (see [[Coulomb's law]]):
$$\begin{flalign}  &\nabla \cdot \vec{E}(\vec{R}) = \frac{1}{4 \pi \varepsilon_{0}} \int\limits_{V'}^{} \rho(\vec{R'})\nabla \cdot \left( - \nabla \frac{1}{\lvert \vec{R}-\vec{R'} \rvert} \right) \ dv' \\ &\begin{cases} \frac{\rho(\vec{R})}{\varepsilon_{0}}, \ \ \text{ iff } \vec{R} = \vec{R'} \\ 0, \ \ \text{ iff } \vec{R} \neq \vec{R'} \end{cases}\end{flalign}$$
This is Gauss law in point form. We want **integral form** and we apply [[Divergence theorem]] and drop the $\vec{R}$ dependence.

- By choosing a volume $V$ with a closed surface $S$ we calculate LHS and RHS.
$$\begin{flalign} &LHS = \int\limits_{V}^{} \nabla \cdot \vec{E} \ dv \oint\limits_{S}^{} \vec{E} \cdot \ d \vec{s} \\ &RHS = \int\limits_{V}^{} \rho \ dv \end{flalign}$$
whereas the RHS is equal to $Q_{encl}$, which is the total charge enclose in V (or S).
We now get $$\oint\limits_{S}^{} \vec{E} \cdot \ d \vec{s} = \frac{Q_{encl}}{\varepsilon_{0}}$$
**Definition of Gauss law in integral form:** Total outward flux of the electric field over any closed surface in free space is equal to the total charge enclosed in the surface divided by the permittivity in free space $\varepsilon_{0}$.

## Using Gauss law
- Simplifying the calculation for $\vec{E}$ (above).
- If we have symmetry we can simplify LHS.
	  - The symmetry needed is finding a simple enclose surface S where $\lvert \vec{E}  \rvert$ ($=E_{0}$) is constant in magnitude across the surface and normal (perpendicular) in direction to the surface
- By having this we can write $$\oint\limits_{S}^{} \vec{E} \cdot \ d \vec{s} = E_{0} \oint\limits_{S}^{}  \ ds \rightarrow E_{0} = \frac{Q_{encl}}{\varepsilon_{0}\oint\limits_{S}^{}  \ ds}$$
		- But we need to find such S $\rightarrow$ **Gaussian surface**

### Example
Choosing spherical coordinates:
![[Pasted image 20221005111457.png]]
We now get: $$\begin{flalign}  &LHS = \oint\limits_{S}^{} \vec{a}_{r}E_{0} \cdot \vec{a}_{R} \ ds = E_{0} \oint\limits_{S}^{}  \ ds = 4\pi R^{2}E_{0} \\ &RHS = \frac{Q_{encl}}{\varepsilon_{0}} = \frac{q}{\varepsilon_{0}} \Rightarrow \vec{E} = \vec{a}_{R}E_{0} = \frac{1}{4 \pi \varepsilon_{0}} \frac{q}{R^{2}}\vec{a}_{R} \end{flalign} $$
we can see [[Coulomb's law]].

### Conclusion of different charges
- Point charge (like example above) - $\frac{1}{R^{2}}$ decay
- Line charge - $\frac{1}{R}$ decay
- Planar charge - no decay



