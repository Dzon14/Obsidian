---
tags: [el]
aliases: [magnetic force]
---
# Magnetic forces
As shown in [[Biot-Savart law]], for a charge q moving at velocity $\vec{u}$ at P in $\vec{B}$ field, it experiences a magnetic force $\vec{F}_{m} = q \vec{u} \times \vec{B} \ \ [N]$.
Now we want to translate the moving charge q to electric current $I$.

Consider a small $d \vec{l}$ of a current carrying conductor with N charge carriers per unit volume moving at drift velocity $\vec{u}$ in the direction $d \vec{l}$.
![[Pasted image 20221128114002.png]]
To conclude the derivation: 
- The force is $d \vec{F}_{m} = I \ d \vec{l} \times \vec{B} \ \ [N]$
- Closed loop: $\vec{F}_{m} = I_{1} \oint\limits_{C_{1}}^{} d \vec{l}_{1} \times \vec{B} \ \ [N]$
- Two-circuit system: $\vec{F}_{21} = I_{1} \oint\limits_{C_{1}}^{} d \vec{l}_{1} \times \vec{B}_{21} \ \ [N]$

Using [[Biot-Savart law]] we get the [[Ampere's force law]]: $$\vec{F}_{21} = \frac{\mu_{0}I_{1}I_{2}}{4 \pi} \oint\limits_{C_{1}}^{} \oint\limits_{C_{2}}^{} \frac{d \vec{l}_{1} \times (d \vec{l}_{2} \times \vec{a}_{R_{21}})}{R_{21}^{2}} \ \ \ [N]$$
## Example
![[Pasted image 20221128115008.png]]

## Example 2 - uniform $\vec{B}$ field
Here, [[torque]] is introduced
![[Pasted image 20221128143605.png]]
![[Pasted image 20221128144317.png]]