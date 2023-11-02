---
tags: [el]
---
# Charge redistribution based on equation of continuity
To ensure $\rho= 0$ and $\vec{E} = 0$

For Ohmic material, $$\vec{J} = \sigma \vec{E} \Rightarrow \nabla \cdot \vec{J} = \nabla \cdot \sigma \vec{E} = - \frac{\partial \rho}{\partial t} \Rightarrow \nabla \vec{E} = - \frac{1}{\sigma}\frac{\partial \rho}{\partial t}$$
If ohmic material is linear [[dielectrics|dielectric]] we get $\vec{D} = \varepsilon \vec{E}$.
Substituting into [[Gauss law]] in point form gives: $$\nabla \cdot \vec{D} = \rho \Leftrightarrow \nabla \cdot \varepsilon \vec{E} \Leftrightarrow \nabla \cdot \vec{E} = \frac{\rho}{\varepsilon}$$
Combining these equations we get $$- \frac{1}{\rho}\frac{\partial \rho}{\partial t} = \frac{\rho}{\varepsilon} \Leftrightarrow \frac{\partial \rho}{\partial t} + \frac{\sigma}{\varepsilon} \rho = 0$$
The solution is $$\rho (t) = \rho_{0} e^{-\frac{\sigma}{\varepsilon}t}$$ where $\tau = \frac{\varepsilon}{\sigma}$ is the **time constant** (the time needed to decrease the value of the function to $\rho_{0}e^{-1}$). $e^{-1} \approx 0,37$

## Example
Copper. What is the time constant?
$\varepsilon = 8.85 \times 10^{-12} \approx \varepsilon_{0} \ \ [F/m]$
$\sigma = 5.8 \times 10^{7} \ \ [S/m]$
$$\tau = \frac{\varepsilon}{\sigma} = 1.52 \times 10^{-19} \ \ [s] \Rightarrow \text{any } \rho_{0} \neq 0 \text{ will disperse}$$

#### What about perfect conductor?
$$\begin{cases}  \varepsilon \approx \varepsilon_{0}, \ \ \text{(the same)} \\ \sigma \rightarrow \infty \end{cases}$$
tvärtom för poor conductors