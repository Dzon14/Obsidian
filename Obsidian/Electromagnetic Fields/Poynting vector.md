---
tags: [el]
---
# Poynting Vector 

Poynting vector in *time domain* $\mathcal{P}(\vec{R},t)$ defines the magnitude and direction of power flow per unit area: $$\mathcal{P}(\vec{R},t) = \vec{E}(\vec{R},t) \times \vec{H}(\vec{R},t) \ \ \ [W/m^{2}]$$Derived from the Law of Energy Conservation.

**Poynting theorem:** $$\oint\limits_{S}^{} (\vec{E} \times \vec{H}) \cdot \ d \vec{s} = - \frac{\partial}{\partial t} \int\limits_{V}^{} (\frac{1}{2}\varepsilon E^{2} + \frac{1}{2} \mu H^{2}) \ dv - \int\limits_{V}^{} \sigma E^{2} \ dv \ \ \ [W] \equiv \text{ Poynting Theorem}$$
- $(\vec{E} \times \vec{H}) = \mathcal{P}(\vec{R},t)$.
- $\frac{1}{2} \varepsilon E^{2}$ and $\frac{1}{2} \mu H^{2}$ are electric and magnetic energy densities (at a point)
- $\int\limits_{V}^{} \sigma E^{2} \ dv$ is basically [[Joule's law]], which gives the total power dissipated in a volume $V$ due to collisions of electronc with atoms 
$\Rightarrow P = \int\limits_{V}^{} \vec{E} \cdot \vec{J} \ dv$, with $\vec{J} = \sigma \vec{E}$.
$\sigma E^{2}$ is called **Ohmic power density.**
![[Pasted image 20221205135713.png]]

## Poynting Theorem described in words
In words, Poynting Theorem states that net power flow out of closed surface $S$ = negative rate of increase of electric and magnetic energies minus the power dissipated as heat due to conductivity of material. It can be seen as an extension of  [[Joule's law]] to time-varying fields. (Note: Though presented in the context of plane waves, the expression $\mathcal{P}(\vec{R},t)$ apply in general to time varying $\vec{E}$ and $\vec{H}$ fields.)
