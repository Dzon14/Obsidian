---
tags: [el]
---
# Method of Images 
If charge distribution is lnown everywhere, we can calculate [[Electric potential]] $V$ and [[Electric field]] $\vec{E}$. But if not, we cannot find $V$ or $\vec{E}$ using any of the methods taught in the course so far! 
However, when conducting bodies have boundaries of a simple geometry, we can replace these boundaries by image (equivalent) charges to satisfy the equipotential [[boundary conditions for electrostatic fields|boundary condition]] of [[Conductor|conductors]] (e.g. $V_{0}= 0$ if grounded). Note that the image charges are NOT real, similar as the idea of surface and volume densitites of bounded charges used to describe the [[Polarisering|polarization]] of a [[dielectrics|dielectric]] in an [[Electric field]] ([[Elmagi F7]]).

Method of images is an example application of the uniqueness theorem, i.e. a solution of an electrostatic problem satisfying its boundary conditions is the only possible solution (even if obtained by an intelligent guess).

## Example 1 
- A point chargr +q is at a distance d from an infinitely large grounded conducting plane (in vacuum). Find $V$ or $\vec{E}$ above the plane. 
- What is the surface charge distribution on the grounded conducting plane?
- How to use the method of images? We need to ensure that the [[boundary conditions for electrostatic fields|boundary condition]]
$V_{0}= 0$ is satisfied. Where shoulde we place the "image charge", at a mirror image location?

Now we can find $\vec{E}$ (or $\vec{D}$) and also surface charge distribution, e.g. at point a point $P_0$ on the plane, between +q and -q.
Based on the real and image charges, $$\vec{D} = - \vec{a}_{n} \frac{q}{4 \pi d^{2}}+ \vec{a}_{n}\frac{-q}{4 \pi d^{2}}= -\vec{a}_{n}\frac{q}{2 \pi d^{2}}$$
But we know from [[Elmagi F8]] that $$D_{1n} = \rho_{s}= \varepsilon_{0}E_{1n} \Rightarrow \rho_{s}= ????$$

## Example 2
- A point charger near the corner of two right-angled infinite grounded plane. Find the locations of the image charges.
**Inser picture**

Note: In general, the angle between the two planes can be $\alpha = \frac{360\degree}{M}$ , where M is an even number (Example 1 is the special case with M = 2 and Example 2 is the special case with M = 4) . Then, M −1 image charges can be used to achieve $V_{0}= 0$ at the boundary.

## Example 3 
- An [[electric dipole]] above an infinite grounded plane. Find the image charge locations.
**Insert picture**

## Example 4
- A point charge outside a grounded spherical conductor of radius $a$. Find the location and magnitude of the image charge. 
**Insert picture**

At point $M$, $$\begin{align} V_{M}= \frac{1}{4 \pi \varepsilon_{0}} \left(\frac{q}{R} + \frac{q_{i}}{Ri} \right) = 0 \ \text{ (boundary condition) } \\ \Leftrightarrow \frac{q}{R}= - \frac{q_{i}}{R_{i}} \Leftrightarrow \frac{R_{i}}{R}= -\frac{q_{i}}{q} \text{ (a constant)} \end{align}$$
**Beware:** $\vec{E}$ found from method of images is only valid for points above the boundary (in the same region as the real charge(s), see examples 1-3), since $\vec{E} =0, \ V_{0}=0$ underneath (shielded region).
**Demo:** http://demonstrations.wolfram.com/MethodOfImagesInElectrostatics/

## Recipe

1) Make an initial guess of the positions(s) of the image charge(s).
2) If needed, use the [[boundary conditions for electrostatic fields|boundary condition]] (e.g., $V_{0}=0$) to find the exact position(s) and magnitude of the charge(s), e.g. the case of point charge outside a grounded sphere.
3) Once the image charge(s) is found, then use it together with the real chrage(s) to determine the $\vec{E}$ field everywhere outside the conductor. 