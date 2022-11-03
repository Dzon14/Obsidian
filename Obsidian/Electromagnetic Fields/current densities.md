---
tags: [el]
---
# Current densities 
For a given free charge carrier, each charge $q$ flows steadily across a surface $\Delta \vec{s}$ with drift velocity $\vec{u}$, as illustrated below
![[Pasted image 20221103140010.png]]
Then, the total amount of charges passing through the surface $\Delta \vec{s}$ in time $\Delta t$ is given by : $$\Delta Q = Nq \vec{u} \Delta t \cdot \Delta \vec{s} \ \ [C]$$where,
- $N \equiv \text{number of charges per unit volume}$
- $\vec{u} \Delta t \equiv \text{displacement of each charge in time} \Delta t$ 
- $\Delta \vec{s} = \vec{a}_{n} \Delta s \equiv \text{vector surface of magnitude }\Delta s \text{ and direction } \vec{a}_{n} \ (\text{normal to surface } \Delta s)$ 
Therefore, the flow of charges through $\Delta \vec{s}$ per unit time $\Delta t \equiv \text{electric current passing through } \Delta \vec{s}$, i.e., $$\Delta I = \frac{\Delta Q}{\Delta t} = Nq \vec{u} \cdot \Delta \vec{s} \ \ [Cs^{-1} \text{ or } A]$$
Define the current density vector $\vec{J} \overset{\Delta}{=} Nq \vec{u} \ \ [Am^{-2}]$ 
This allows us to write: $$\Delta I = \vec{J} \cdot \Delta s \ \ [Cs^{-1} or A]$$The current passing through the entire surface S is then: $$I = \int\limits_{S}^{} \vec{J} \cdot \ d \vec{s} \ \ [A]$$For **conduction currents**, we can have more than one type of charge carriers in general, therefore the *net* current density from all charge carriers is: $$\vec{J} = \sum\limits_{i}^{}N_{i}q_{i} \vec{u}_{i} \ \ [Am^{-2}]$$

How do we relate $\vec{J}$ to applied $\vec{E}$ (cause of charge carrier flow)?
- For most conducting materials in the real world (not perfect conductors), the average drift velocity of the charge carrier(s) is proportional to the applied [[Electric field]] $\vec{E}$ i.e. $\vec{u} \propto \vec{E}$.

Why do we have constant drift velocity $\vec{u}$ for a given $\vec{E}$?
- From our study of [[Electrostatics]], we would have expected that a constant force is exerted on a static charge $q$ due to $\vec{E}$.

In metal conductors with electroncs being the charge carrier: $\vec{u} = - \mu_{e}\vec{E}$, where $\mu_{e} \equiv \text{mobility of electrons, eq. } \mu_{e}(Cu) = 3.2 \times 10^{-3} \ \ [m^{2}/Vs]$

**Demo:**
http://demonstrations.wolfram.com/ElectricCurrent/