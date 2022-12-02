---
tags: [el]
aliases: [capacitor]
---
# Capacitance
(Note: Capacitance and capacitor is not the same thing. Capacitor is a passive device whilst capacitance is the property of a capacitor).
- Capacitance is a physical property of the two-conductor system
- The system is separated by vacuum or [[dielectrics]].

Concept of capacitance of one or more conductors derived from the relationship between electric charges $Q$ and the [[electric potential]] $V$.
![[Pasted image 20221012112054.png]]
Increasing $Q \Rightarrow$ proportional increase in $\rho_{s}(\vec{R}')(Q \propto \rho_{s})$ as charge distribution **does not** change
At point P, $$V = \frac{1}{4 \pi \varepsilon_{0}} \oint\limits_{S'}^{} \frac{\rho_{s}(\vec{R}')ds'}{\lvert \vec{R} -  \vec{R}'\rvert}$$
Point P can be on the conduction (equipotential).
We also get
$$\begin{flalign} \Rightarrow &Q \propto V \\ &Q = C V  \end{flalign}$$
where C is capacitance - in farad $[F]\ / \ [\frac{C}{V}]$.

In this case, $C = \frac{Q}{V_{12}}$, where $V_{12}$ is the potential differene between the two conductors.

## [[How to find the capacitance]]

## 3 or more [[Conductor|conductors]]
In general we consider an N-[[Conductor]] system in an isolated system. The charges from all conductors contribute to the [[electric potential]] in each conductor. 
$$V_{N} = p_{N1}Q_{1}+p_{N2}Q_{2} + \text{... }+ p_{NN}Q_{N}$$whereas $p_{ij} \equiv \text{coefficients of potential}$, or in terms of charges $$Q_{N} = c_{N1}V_{1}+c_{N2}V_{2}+ \text{ ... } + c_{NN}V_{N}$$where $c_{ii} \equiv \text{coefficients of capacitance}$ and $c_{iy}(i \neq j) \equiv \text{coefficients of induction}$.  

- How do we relate coefficients of capacitance and induction to coupling capacitance of two conductors? For a 3-conductor system, conductor 0 is conducting earth at $V_{0}= 0$.
![[Pasted image 20221101105116.png]]
![[Pasted image 20221031163417.png]]

## Example of capacitance calculation for N-conductor system
Consider a physical 3-conductor system in vacuum, where conductors 1 and 2 are the inner and outer concentric spherical shells, and conductor 0 is grounded at infinity with $V_{0} = 0 \ [V]$. 

Following the multi-conductor convention, we place $Q_{1}$ on the inner shell (conductor 1) and $Q_{2}$ on the outer shell. To find capacitance, use [[Gauss law]] (Find $\vec{E}$) and $V_{ab} = - \int\limits_{b}^{a} \vec{E} \cdot \ d \vec{l}$ : $$R \geq R_{o} \text{ , } \ \ \vec{E}= \vec{a}_{R} \frac{Q_{1} + Q_{2}}{4 \pi \varepsilon_{0}R^{2}} \Rightarrow V = - \int\limits_{\infty}^{R} \frac{Q_{1}+Q_{2}}{4 
 \pi \varepsilon_{0}R^{2}}\vec{a}_{R} \cdot \ (\vec{a}_{R}dR) = \frac{Q_{1}+Q_{2}}{4 \pi \varepsilon_{0}R}$$
 Similarly, $$ \begin{flalign} &R_{i} \leq R \leq R_{0}, \ \ \vec{E}(R) = \vec{a}_{R}\frac{Q_{1}}{4 \pi \varepsilon_{0}R^{2}} \\ &\Rightarrow V(R) = - \int\limits_{p_{i}}^{p_{f}} \vec{E} \cdot \ d \vec{l} = - \int\limits_{\infty}^{R_{o}} \frac{Q_{1} + Q_{2}}{4 \pi \varepsilon_{0}R^{2}}\vec{a}_{R} \cdot \ (\vec{a}_{R}d \vec{l}) - \int\limits_{R_{o}}^{R} \frac{Q_{1}}{4 \pi \varepsilon_{0}R^{2}}\vec{a}_{R} \cdot \ (\vec{a}_{R}d \vec{l}) \\ &= \frac{Q_{1}+Q_{2}}{4 \pi \varepsilon_{0}R_{o}} + \frac{Q_{1}}{4 \pi \varepsilon_{0}}\left(\frac{1}{R}- \frac{1}{R_{o}}\right) = \frac{Q_{1}}{r \pi \varepsilon_{0}R}+\frac{Q_{2}}{4 \pi \varepsilon_{0}R_{o }}\end{flalign}$$ and $0 \leq R \leq R_{i}, \ \ \vec{E} = 0 \Rightarrow V = \frac{Q_{1}}{4 \pi \varepsilon_{0} R_{i}}+\frac{Q_{2}}{4 \pi \varepsilon_{0}R_{o}}$ (equipotential in inner volume).
Therefore, on conductor 1 ($R=R_{i}$),   $V_{1} = \frac{Q_{1}}{4 \pi \varepsilon_{0} R_{i}}+\frac{Q_{2}}{4 \pi \varepsilon_{0}R_{o}}$
On conductor 2 ($R = R_{o}$),   $V_{2}= \frac{Q_{1}+Q_{2}}{4 \pi \varepsilon_{0}R_{o}}$
![[Pasted image 20221031202138.png]]
- **Comparing** with the circuit model:
$$\begin{align} c_{11} &= C_{10}+C_{12} \\ c_{12} &= -C_{12} \\ c_{22} &= C_{20}+C_{12} \end{align}$$
So we know $C_{12}= \frac{4 \pi \varepsilon_{0}R_{i}R_{o}}{R_{o}-R_{i}}$ (similare to capacitance of spherical capacitor with $R_{i} \text{ and }R_{o}$ as inner and outer radii, respectively, but here $\varepsilon= \varepsilon_0$, see [[Elmagi F8]]).
This gives $C_{10}= c_{11} - C_{12}= 0$ and $C_{20}= c_{22}-C_{12} = \frac{4 \pi \varepsilon_{0}R_{o}^{2}}{r_{o}-R_{i}}- \frac{4 \pi \varepsilon_{0}R_{i}R_{o}}{R_{o}-R_{i}} = 4 \pi \varepsilon_{0}R_{o}$

- This example shows how capacitances can be explicitly calculated, both the coefficients of capacitance and induction, and the partial capacitances (for an equivalent circuit model).