---
tags: [el]
---
# Ampere's Circuital Law

### Integral form
Ampere's circuital law in **integral form**: $$\oint\limits_{C}^{} \vec{B} \cdot \ d \vec{l} = \mu_{0}I_{enc}$$where $I_{enc} = \int\limits_{S}^{} \vec{J} \cdot \ d \vec{s}$.  Reminder: $\mu_{0}$ is the magnetic permeability.
The circulation of magnetic flux density in vacuum around any closed path C is equal to $\mu_{0}$ time the total (or net) current flowing through the surface bound by the path. 

In vacuum, $\vec{B} = \mu_{0}\vec{H}$, where $\vec{H}$ is magnetic field intensity with the unit $[A/m]$.
$$\Rightarrow \oint\limits_{C}^{} \vec{H} \cdot \ d \vec{l} = I$$

- Ampere's Circuital Law (both integral and point form) is **derived** from [[Biot-Savart law]] and using [[Curl]] etc.

##### How do we use it?
$\oint\limits_{C}^{} \vec{B} \cdot \ d \vec{l} = \mu_{0}I_{enc}$
- Find an Amperian loop C - the loop C to fulfill the symmetry conditions
- $\lvert \vec{B} \rvert$ constant along C
- $\vec{B} || d \vec{l}$ along C
You can only use the aw if you know the entire circuit, since there must be symmetry. Don't use it if you only know about a part/section of the circuit. 

### Point form 
When deriving we first get Ampere's circuital law in **point form** which is $$\begin{align} \nabla \times \vec{B}(R) = \frac{\mu_{0}}{4 \pi} \int\limits_{V'}^{} \vec{J}(\vec{R}')4 \pi \delta (\lvert \vec{R} - \vec{R}' \rvert) \ dv' 
= \begin{cases} \mu_{0}\vec{J}(\vec{R}), \ \ \ \text{ iff } \vec{R}= \vec{R}' \\ 0, \ \ \ \ \ \ \ \ \ \ \ \ \ \ \text{ iff } \vec{R} \neq \vec{R}' \end{cases} \end{align}$$
To get the integral form we apply [[Surface integral]] and [[Stoke's theorem]].


## Example 1
![[Pasted image 20221114104955.png]]
where $$(*) = B_{\phi} 2 \pi r = \mu_{0}I \Leftrightarrow B_{\phi} = \frac{\mu_{0}I}{2 \pi r} \Rightarrow \vec{B} = \frac{\vec{a}_{\phi}\mu_{0} I }{2 \pi r} \ \ [T]$$
## Example 2
![[Pasted image 20221114105412.png]]
**i) Inside cavity$**, $r < a$
- $I_{enc} = 0$
- $\oint\limits_{C}^{} \vec{B} \cdot \ d \vec{l} = B_{\phi}2 \pi r \Rightarrow \vec{B} = 0$

**ii) Inside conductor**, $a \leq r \leq b$
- $I_{enc} = \frac{I \pi (r^{2}-a^{2})}{\pi (b^{2} - a^{2})} \Rightarrow$
- $\Rightarrow \vec{B} = \vec{a}_{\phi} \frac{\mu_{0}I(r^{2}-a^{2})}{2 \pi r (b^{2}-a^{2})} \ \ [T]$

**iii) Outside conductor**, $r > b$
- $I_{enc} = I$
- $\Rightarrow \vec{B}= \vec{a}_{\phi} \frac{\mu_{0}I}{2 \pi r}$

