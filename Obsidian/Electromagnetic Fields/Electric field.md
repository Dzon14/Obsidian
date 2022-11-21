---
aliases: [field]
tags: [el]
---
# Electric field
Based on electric force. If we want to know the force on a test charge ($q_0$), due to a given charge ($q_1$), the answer is [[Coulomb's law]]

We **define** it as $$\lvert \vec{E} \rvert = \frac{\lvert \vec{F_{10}} \rvert}{q_{0}} = \frac{1}{4 \pi \varepsilon_{0}}\frac{q_{1}}{R^{2}_{10}}\lvert \vec{a}_{R_{10}} \rvert$$
#### Visualization 
![[Pasted image 20220919113612.png]]
- The origin and the **source point** is not the same thing. 
- ![[Pasted image 20220919113808.png|400]]
- Our unit vector becomes $$\vec{a}_{R^{''}} = \frac{\vec{R}-\vec{R'}}{\lvert \vec{R}-\vec{R'} \rvert}$$
and we get $$\vec{E} = \frac{1}{4 \pi \varepsilon_0}\frac{q_{1}}{\lvert \vec{R}-\vec{R'} \rvert} \vec{a_{R''}}$$
For more than one charge: $$\begin{align} \vec{E} = \frac{1}{4 \pi \varepsilon} \sum_{k=1}^{n}\frac{q_{k}(\vec{R}-\vec{R}'_k)}{\lvert \vec{R}-\vec{R'_k} \rvert} \\ \\ \vec{F} = q_{0}\vec{E} \end{align}$$
### $\vec{E}$ for distributed charges
- If the charges are not single point charges, but distributed along a line, surface, or volume
$$d \vec{E} = \vec{a}_{R} \frac{dq_{0}}{4 \pi \varepsilon_{0}R^{2}}$$
- For volume charges of charge density p. $$\vec{E} = \frac{1}{4 \pi \varepsilon_{0}}\int_{V'}^{} \vec{a}_{R}\frac{p}{R^{2}} \ dv'$$
![[Pasted image 20220919114800.png|600]]


- For a positive charge the electric force will be in the same direction as the field.
- For a negative charge the electric force will be in the same direction as the field. 