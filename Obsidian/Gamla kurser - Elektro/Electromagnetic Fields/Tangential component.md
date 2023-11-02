---
tags: [el]
---
# Tangential component
We find the [[boundary conditions for electrostatic fields|boundary condition]] for this by using concept of potential difference.
![[Pasted image 20221012103113.png]]
for a small closed loop $C$ , $$\Delta V = - \oint\limits_{abcda}^{} \vec{E} \cdot \ d \vec{l} = V(a) - V(a)=0$$
$$\oint\limits_{abcda}^{} \vec{E} \cdot \ d \vec{l} = \left[\int\limits_{ab}^{}  + \int\limits_{bc}^{}   + \int\limits_{cd}^{} + \int\limits_{da}^{}   \right] \vec{E} \cdot d \vec{l} = 0$$
If $\Delta h \rightarrow 0$ (to study $\vec{E}$ very close to the boundary) we approximate $\left[ \int\limits_{bc}^{} + \int\limits_{da}^{} \right]\vec{E} \cdot d \vec{l}=0$

The curve integral is now the two remaining side which is $$\oint\limits_{abcda}^{} \vec{E} \cdot \ d \vec{l} = \vec{E} \cdot \Delta \vec{w} + \vec{E}_{2} \cdot (- \Delta \vec{w}) = (\vec{E}_{1}-\vec{E}_{2}) \cdot \Delta \vec{w} = 0$$
$\Rightarrow$ we get the **Tangential component** of the [[Electric field]] $\vec{E}$ , and it's **continous** across the boundary.
**Note:**
1) When medium 1 is a conductor, then $\vec{E}=0$ (inside conductor) $\Rightarrow$ $E_{1t} = 0 \Rightarrow E_{2t}=0$, same if material 2 is conductor
2) When both media 1 and 2 are linear [[dielectrics]], $\vec{D} = \varepsilon \vec{E}$, and so $E_{1t}=E_{2t} \Leftrightarrow \frac{D_{1t}}{\varepsilon_{1}} = \frac{D_{2t}}{\varepsilon_{2}}$, where $\varepsilon_{1} \neq \varepsilon_{2}$
3) Concept of [[Electric potential]] useful even here!