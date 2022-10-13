---
tags: [el]
---
# How to find the capacitance
$$C = \frac{Q}{V_{12}}$$$V_{12}$ is the potential difference between the two conductors.
- Start with finding $\vec{E}$, then $V_{12}$ and finally $C$

## Recipe
1) Choose a coordinate system to find $\vec{E}$.
2) Assume $+Q$ and $-Q$ on the conductors 1 and 2, respectively.
3) Find $\vec{E}$ inside capacitor from $Q$ (e.q. two helpful tools or direct calculations)
4) FInd $V_{12} = -\int\limits_{-Q \rightarrow +Q}^{} \vec{E} \cdot  \ d \vec{l}$   ( from conductor 2 to conductor 1, should be $+ve$).
5) Find $C = \frac{Q}{V_{12}}$

## Example 1 - Parallel plate capacitor
1) Cartesian
2) Assume..
3) Find $\vec{E}$ from $Q$.
Constant field inside the capacitor. ($\vec{D}= \varepsilon \vec{E}$)From deriving the [[Normal component]] of the [[boundary conditions for electrostatic fields|boundary condition]] using [[Gauss law]] we know that $$\lvert \vec{D} \rvert = \rho_{s} \Rightarrow \vec{D} = -\vec{a}_{y}\rho_{s} \Rightarrow \vec{E} = - \vec{a}_{y} \frac{\rho_{s}}{\varepsilon}$$
4) $$V_{12} = - \int\limits_{-Q \rightarrow+Q}^{} \vec{E} \cdot \ d \vec{l} = - \int\limits_{0}^{d} \vec{E} \cdot \vec{a}_{y} \ dy = \frac{\rho_{s}}{\varepsilon} \int\limits_{0}^{d} dy = \frac{\rho_{s}d}{\varepsilon} = [\rho_{s}=\frac{Q}{S}]= \frac{Qd}{S \varepsilon}$$
5) $C = \frac{Q}{V_{12}}= \varepsilon \frac{S}{d}$


## Example 2 - Cylindrical capacitor
Lecture 8

## Example 3 - Spherical capacitor (self-reading)
Lecture 8