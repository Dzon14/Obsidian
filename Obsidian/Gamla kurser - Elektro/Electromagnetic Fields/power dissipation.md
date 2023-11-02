---
tags: [el]
---
# Power Dissipation
The proportionality $\vec{u} \propto \vec{E}$ in a real conducting material implies that the electrons do not experience free movement through the material. Instead, they collide with the atoms in the material. 
The collisions result in transfer of energy from work done on the charges to the heat dissipated in the material. 

Wor kdone by a single charge q in field $\vec{E}$ over displacement $\Delta \vec{l}$: $$\Delta w = force \times distance = \vec{F} \cdot \Delta \vec{l} = q \vec{E} \cdot \Delta \vec{l}$$
Therefore, power transferred from one charge q: $$p = \frac{dw}{dt} = \lim_{\Delta t \rightarrow 0}\frac{\Delta w}{\Delta t} = \lim_{\Delta t \rightarrow 0}q \vec{E} \cdot \frac{\Delta \vec{l}}{\Delta t} = q \vec{E} \cdot \vec{u}$$
For charge carrier i, the power transferred per unit volume is then: $$p_{i} = N_{i}q_{i}\vec{E} \cdot u_{i} = \vec{E} \cdot (N_{i}q_{i}\vec{u}_{i})$$
where $N_{i} \equiv$ number of charges per unit volume for charger carrier i.

For volume dv, the power transferred from all charge carriers is $$dP = \left(\sum\limits_{i}^{}p_{i} \right)dv = \vec{E} \cdot \left( \sum\limits_{i}^{}N_{i}q_{i} \vec{u}_{i} \right)dv = \vec{E} \cdot \vec{J} dv$$
$$\Rightarrow \frac{dP}{dv} = \vec{E} \cdot \vec{J}$$which is called **power density in point form**.

At a macroscopic level, we can consider the total dissipated power in a volume V:$$\Rightarrow P = \int\limits_{V}^{} \vec{E} \cdot \ dv \ \ \ [W]$$which is called [[Joule's law]].