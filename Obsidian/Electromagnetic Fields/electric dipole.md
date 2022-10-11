---
tags: [el]
---
# Electric dipole
We define **electric dipole moment** $$\vec{p} \overset{\Delta}{=}q \vec{d} \Rightarrow V = \frac{\vec{p} \cdot \vec{a}_{r}}{4 \pi \varepsilon_{0}R^{2}}$$
But $\vec{p}$ is defined for a single dipole. in a volume $\Delta v$ of a [[dielectrics|dielectric]] material with n induced dipoles we can define the polarization vector $$\vec{P} \overset{\Delta}{=} \lim_{\Delta v\to 0}\frac{\sum\limits_{k=1}^{n \Delta v}\vec{p}_{k}}{\Delta v} \equiv \text{ volume density of electric dipole moment}$$
### How does $P$ contribute to [[Electric potential]]?
By rewriting $d \vec{p}$, the differential potential $dV$ etc. we get $$V = \frac{1}{4 \pi \varepsilon_{0}} \oint\limits_{S'}^{} \frac{\vec{P} \cdot \vec{a}_{n}'}{R} \ ds' \ + \ \frac{1}{4 \pi \varepsilon_{0}} \int\limits_{V'}^{} \frac{(- \nabla' \cdot \vec{P})}{R} \ dv'$$
where $$\begin{cases} \rho_{ps} \overset{\Delta}{=} \vec{P} \cdot \vec{a}_{n} \equiv \text{ surface charge density } \\ \rho_{p} \overset{\Delta}{=} (- \nabla \cdot \vec{P}) \equiv \text{ volume charge density} \end{cases}$$
where they both are polarization or bounded charge densities.

## [[Electric field]] from a dipole
$$\vec{E} = \frac{p}{4 \pi \varepsilon_{0}R^{3}} 2cos \theta \ \vec{a}_{R} + sin \theta \ \vec{a}_{\theta}$$
