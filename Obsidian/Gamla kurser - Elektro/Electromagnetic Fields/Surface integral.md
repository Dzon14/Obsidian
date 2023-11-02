---
tags: [matte]
---
# Surface integral
Can be closed or open

To measure how many equivalent field lines of the field $\vec{A}$ (e.g. electric field $E$) pass through a given surface, we define the total **outward flux** (or field lines) of the [[vector field]] through **S** as: $$\int_{S}^{} \vec{A} \cdot \ d \vec{s}$$
where $d \vec{s} = \vec{a}_{n}ds$
![[Pasted image 20220926112344.png|200]]
The normal unit vector $\vec{a}_{n}$ points "outwards" from the surface.

$$\begin{align}  \vec{D} \overset{\Delta}{=} \text{Electric flux/electric displacemenet} \\\vec{D} = \varepsilon_{0}\vec{E}\end{align}$$
and the outward electric flux is defined as $$\Phi_{e} \overset{\Delta}{=} \int_{S}^{} \vec{D} \cdot \ d \vec{s}$$
To evaluate a surface intergral numerically:
1. Choose a suitable coordinate system
2. Form the surface element $d \vec{s}$
3. Perform the integral

### Example
- Spherical coordinate system!
- Direction: $d \vec{s} = \vec{a}_{R} ds = \vec{a}_{R}dl_{\theta} dl_{\phi} = \vec{a}_{R}R d \theta R sin \theta d \phi$

$$\vec{E} = \frac{q}{4 \pi \varepsilon_{0} R^{2}}\vec{a}_{R}$$
so we get
 $$\oint_{s}^{} \vec{E} \cdot \ d \vec{s} = \frac{q}{4 \pi \varepsilon_{0}} \int_{0}^{2 \pi} \int_{0}^{\pi} \frac{1}{r^{2}}R^{2}sin \theta \ d \phi \ d \theta = \frac{q}{\varepsilon_{0}}$$

 