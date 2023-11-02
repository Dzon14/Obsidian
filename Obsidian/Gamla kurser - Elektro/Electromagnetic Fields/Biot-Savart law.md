---
tags: [el]
---
# Biot-Savart Law
[[Coulomb's law]] tells us the force exerted by two static point charges on each other.
We can write the electric force as $\vec{F}_{e}=q \vec{E}$, where q is a test charge.
If we let the charges go free they will start to accelerate away from eachother....
Two freely moving point charges will in general experience **both** an electric force and a magnetic force, as their movement both create $\vec{B}$ and caused them to experience magnetic force.

## Relationships in Biot-Savart law
$$\begin{align} \lvert \vec{F}_{m}\rvert \propto I \\ \\ \lvert \vec{F}_{m} \rvert \propto \frac{1}{R^{2}} \end{align}$$(notice similiraties to [[Coulomb's law]])

## Magnetic force
![[Pasted image 20221109134622.png]]
$$\lvert d \vec{F}_{m} \rvert = k \frac{mIdl'}{R^{2}}sin \alpha$$, where $dl'$ is the length element and $k$ is the proportionality constant.
Due to current flow there were further refinements of the expression leading to $$\vec{B} = \frac{\mu_{0}I}{4 \pi} \oint\limits_{C'}^{} \frac{d \vec{l}' \times \vec{a}_{R}}{R^{2}} \ \ \ \ [T] \text{ or } [Wb/m^{2}]$$which is the magnetic flux density (at point P).
$\mu_{0}= 4 \pi \times 10^{-7}$ is the **pemeability** constant in vacuum (free space).
Remember:  $\vec{a}_{R}= \frac{\vec{R}-\vec{R}'}{\lvert \vec{R}-\vec{R}' \rvert}$
![[Pasted image 20221109135011.png]]
**Notes:**
- Speed of electromagnetic wave in vacuum is $c_{0}= \frac{1}{\sqrt{\mu_{0}\varepsilon_{0}}}$
- Here we assume a closed electrical circuit of thin wire. In general we can write **Biot-Savart law** in terms of current densities as $$\vec{B}(R) = \frac{\mu_{0}}{4 \pi} \int\limits_{V'}^{} \frac{\vec{J}(\vec{R}')\times \vec{a}_{R}}{R^{2}} \ dv' \ \ \ \ [T]$$
Then magnetic focec on a charge q moving at velocity $\vec{u}$ in $\vec{B}$ is $\vec{F}_{m}= q \vec{u} \times \vec{B} \ \ \ [N]$

In general the total force on a given charge moving at velocity $\vec{u}$ is given by $$\vec{F}_{total}= \vec{F}_{e}+\vec{F}_{m}=q(\vec{E}+\vec{u} \times \vec{B}) \ \ \ [N]$$This is known ad the [[Lorentz' force equation]].