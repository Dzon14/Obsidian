---
tags: [el]
aliases: [plane waves, plane wave]
---
# Plane Waves in Lossless Media

In previous lecture the solution for $\vec{E}$ was based on potential functions since it is not convenient to solve for $\vec{E}$ directly. However, for plane waves in a source-free region, it is relatively simple to approach it directly.

We have the following [[wave equations|wave equation]]: $$\nabla^{2} \vec{E} - \frac{1}{c^{2}}\frac{\partial^{2} \vec{E}}{\partial t^{2}} = \frac{1}{\varepsilon_{0}} \nabla \rho + \mu_{0} \frac{\partial \vec{J}}{\partial t}$$where $\frac{1}{c^{2}} = \mu_{0} \varepsilon_{0} \Rightarrow c= \frac{1}{\sqrt{ \mu_{0} \varepsilon_{0}}}, \ \ \mu=\mu_{0}, \ \ \varepsilon = \varepsilon_{0}$ (free space).

However, the plane wave is a special case where wavefronts becoms planar (sourc distributed along an infinite plane).

## Solving $\vec{E}$ for plane waves
![[Pasted image 20221205104116.png]]
In time harmonic fields (phasor form) $$\nabla^{2} \vec{E} - \frac{1}{c^{2}}\frac{\partial^{2} \vec{E}}{\partial t^{2}} = 0 \Leftrightarrow \nabla^{2} \vec{E} - \left( \frac{j \omega }{c} \right)^{2} \vec{E}  =0 \Leftrightarrow \nabla^{2} \vec{E} + k_{0}^{2} =0$$where $k_{0} = \frac{\omega}{c} = \omega \sqrt{ \mu_{0} \varepsilon_{0}} \ \ [rad/m]  \equiv$ free space wavenumber

Using cartesian coordinates and for a unform plane wave we can derive the **second order** differential equation $$\frac{d^{2} E_{x}}{dz^{2}}+ k_{0}^{2} E_{x}=0$$with the solution $$E_{x} (z) = E_{x}^{+}(z) + E_{x}^{-}(z) = E_{0}^{+}e^{jk_{0}z} + E_{0}^{-}e^{jk_{0}z} \ \ \ [V/m]$$
**Note:** By solving for $\vec{E}$ in the source-free region, we solved the hoogeneous wave equations, which provides the form of the solution. To find the exact values of $E_{0}^+$ and $E_{0}^{-}$, we need to solve the non-homogenous wave equation (not equal to 0) with the source terms (not of interest here).

To visualize $E^{+}$ in time domain with $cos \omega t$ as reference phase: $$E_{x}^{+}(z,t)= Re(E_{x}^{+}(z)e^{j \omega t}=E_{0}^{+} cos (\omega t - k_{0}z)$$
The wavelength of the time-harmonic plane wave is given by $\lambda_{0} = \frac{c}{f} = \frac{\omega}{k_{0} f}=\frac{2\pi}{k_{0}}$

By observing $E^{-}$ in the time domain we can conclude that it is the reflected wave travelling in the negative z direction.

## Solving $\vec{H}$ (or $\vec{B}$) field

For the positive z direction the $\vec{H}$ field is $$H_{y}^{+}(z) = - \frac{1}{j \omega \mu_{0}} \frac{\partial E_{x}^{+}(z)}{\partial z} = \frac{k_{0}}{\omega \mu_{0}} E_{x}^{+}(z) = \frac{1}{\eta_{0}}E_{x}^{+}(z)$$where $\eta_{0} = \sqrt{\frac{\mu_{0}}{\varepsilon_{0}}} \approx 377 \ \Omega \equiv$ intrinsic impedance in free space.

In **time-domain:** $$H_{y}^{+}(z,t) = \frac{1}{\eta_{0}}E_{0}^{+}cos(\omega t - k_{0}z)$$
**Note:**
1. These results are valid when the wave is in linear medium with $\mu, \ \varepsilon$.
2. Similar derivations apply to obtain the $E_{y}$ component. However $E_{z}(z,t) = 0$.

**In general**, plane waves can travel in any direction $\vec{a}_{n}$ and we may want to observe the field at an arbitrary point in spave $\vec{R} \equiv$ transverse electromagnetic waves (TEM).

Then $$\vec{E(R)} = \vec{E}_{0} e ^{-j \vec{k}\cdot \vec{R}}$$(where $\vec{k} = \vec{a}_{x}k_{x}+\vec{a}_{y}k_{y}+\vec{a}_{z}k_{z} = k \vec{a}_{n}$) is the *wavenumber vector*. We also get $$\vec{H(R)} = - \frac{1}{j \omega \mu} \nabla \times \vec{E(R)} = \frac{1}{\eta} \vec{a}_{n} \times \vec{E(R)} = \frac{1}{\eta} (\vec{a}_{n} \times \vec{E}_{0})e^{-j \vec{k}\cdot \vec{R}}$$where $\eta = \frac{\omega \mu}{k}$ and $\vec{a}_{n}$ is the direction of wave travel/propagation.
- This gives the general result for the relationship between $\vec{a}_{n}$ and the directions of $\vec{E(R))}$ and $\vec{H(R)}$
- Right hand rule (cross two of the components to get the third. $\vec{H}$, $\vec{E}$ or $\vec{a}_{n}$)

The relationship between the magnitudes of the $\vec{E}$ and $\vec{H}$ fields can be obtained: $$\vec{H}_{0} = \frac{1}{\eta}(\vec{a}_{n} \times \vec{E}_{0}) \Rightarrow \lvert  \vec{E}_{0} \rvert = \eta \lvert \vec{H}_{0} \rvert$$
