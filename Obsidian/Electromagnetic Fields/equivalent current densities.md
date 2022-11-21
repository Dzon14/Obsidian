---
tags: [el]
---
# Equivalent [[current densities]]
We can write [[magnetic dipole moment]] $d \vec{m}$ of an elemental volume $dv' \Rightarrow d \vec{m}=\vec{M} dv'$, which gives a differential [[vector magnetic potential]] at point P: $d\vec{A} = \frac{\mu_{0}d \vec{m}\times \vec{a}_{R}}{4 \pi R^{2}} = \frac{\mu_{0}\vec{M}\times \vec{a}_{R}}{4 \pi R^{2}}dv'$

For a volume of magnetized material $V'$ (and closed surface $S'$), the potential is then: $$\vec{A} = \int\limits_{V'}^{} d \vec{A} = \frac{mu_{0}}{4 \pi} \int\limits_{V'}^{} \frac{\vec{M} \times \vec{a}_{R}}{R^{2}} \ dv'$$After a few more steps and deriving we get $$\vec{A} = \frac{\mu_{0}}{4 \pi} \oint\limits_{S'}^{} \frac{\vec{M} \times \vec{a}_{n}'}{R} \ ds' + \frac{\mu_{0}}{4 \pi}\int\limits_{V'}^{} \frac{(\nabla' \times \vec{M})}{R} \ dv'$$where we have the magnetization or bounded [[current densities]]: $$\begin{align} &\vec{J}_{ms} \overset{\Delta}{=}\vec{M}\times \vec{a}_{n} \ \ [A/m] \equiv \text{ surface current density} \\ &\vec{J}_{m} \overset{\Delta}{=} \nabla \times \vec{M} \ \ [A/m^{2}] \text{ volume current density} \end{align}$$
- Finding $\vec{B}$ (or $\vec{A}$) from a magnetized material $\equiv$ finding equivalent current densities.

**Visualization** of applied external field $\vec{B}_{0}$ causing $\vec{M}$:
![[Pasted image 20221117110009.png|250]]
$$\begin{align} \vec{J}_{ms} &= \vec{M} \times \vec{a}_{n} \neq 0 \\ \vec{J}_{m} &= \nabla \times \vec{M} = 0 \end{align}$$
## Example
![[Pasted image 20221117110209.png|650]]