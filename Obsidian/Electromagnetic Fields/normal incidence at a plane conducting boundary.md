---
tags: [el]
---
# Normal Incidence at a Plane Conducting Boundary

Until now we have considered plane waves travelling in a single (linear, isotropic, homogenous) medium with material properties, $\varepsilon$, $\mu$ and $\sigma = 0$ (lossless medium). In reality, waves can travel across *different* media. 

We consider a plane wave in lossless medium 1 ($\varepsilon_{1}, \mu_{1}$ and $\sigma_{1}=0$, with $\eta_{1} = \sqrt{ \frac{\mu_{1}}{\varepsilon_{1}}}$) incident on a plane perfectly conducting boundary ($\sigma_{2} = \infty$) in the normal direction. 
![[Pasted image 20221207133544.png|550]]

A perfect conductor is equivalent to a perfect diamagnetic material, in which free surface currents will flow in such a way as to ensure $\vec{B} = \vec{H} = 0$ inside the conductor. Similarly we showed that free charges on the surface will be distributed to ensure that $\vec{E} = 0$ in perfect conductors. 
$\Rightarrow$ no penetration of wave and the incident wave is fully reflected ([[Totalreflektion|total reflection]])

If the incident plane wave in time domain is $\vec{E}_{i}(z,t) = \vec{a}_{x}E_{i_{0}}cos(\omega t - k_{1} z)$. Then in phasor form we get the incidents $$\begin{align} &\vec{E}_{i}(z) = \vec{a}_{x}E_{i_{0}}e^{-jk_{1}z} \\ &\vec{H}_{i}(z) = \vec{a}_{y} \frac{E_{i_{0}}}{\eta_{1}}e^{-jk_{1}z}, \ \ \text{ as obtained from } \ \ \frac{1}{\eta} \vec{a}_{n} \times \vec{E}(R) = \vec{H}(R) \end{align}$$**Note:** In Cheng they use phase constant $\beta_1$ instead of wavenumber $k_{1}$. Since lossless media $k_{1} = \beta_{1}$.

Inside *medium 2* , $\vec{E}=\vec{H}= 0$ (perfect conductor). So only reflection possible: $$\begin{align} &\vec{E}_{r}(z) = \vec{a}_{x}E_{r0}e^{jk_{1}z} \ \ \text{ (in medium 1)} \\ \Rightarrow &\vec{E}_{1}(z) = \vec{E}_{i}(z) + \vec{E}_{r}(z) = \vec{a}_{x} \left( E_{i0}e^{-jk_{1}z} + E_{r0}e^jk_{1z} \right) \end{align}$$whereas the latter is the total field.

- At z = 0, $\vec{E}_{2}=0$, since $E_{t}$ continous. No E-field in conductor. Boundary tangential $E_{1t} = E_{2t} = 0$. $\vec{E}_{1}(0) = \vec{E}_{2(0)}\Rightarrow \vec{E}_{1}(0)=0$.  $$\begin{align}  &\Rightarrow E_{r0} = - E_{i0} \\
&\Rightarrow \vec{E}_{r}(z) = -\vec{a}_{x}E_{i0}e^{jk_{1}z} = \vec{a}_{x}E_{r0}e^{jk_{1}z}\end{align}$$This gives $$\vec{H}_{r}(z) = \frac{1}{\eta_{1}}\vec{a}_{n_{r}} \times \vec{E}_{r}(z) = \vec{a}_{y}\frac{E_{i0}}{\eta_{1}}e^{jk_{1}z}$$
We get the **Total field:** $$\begin{align} &\vec{E}_{1}(z) =\vec{E}_{i}(z) + \vec{E}_{r(z)}= \vec{a}_{x}E_{i0} (e^{-jk_{1}z}-e^{jk_{1}z}) = - \vec{a}_{x}j2E_{i0}sink_{1}z \\ &\vec{H}_{1}(z) = \vec{H}_{i}(z) + \vec{H}_{r}(z) = \vec{a}_{y} \frac{2E_{i0}}{\eta_{1}}cosk_{1}z \end{align}$$In time-domain representation: $$\begin{align}  &\vec{E}_{1}(z,t) = Re[\vec{E}_{1}(z) e^{j \omega t}] = \vec{a}_{x}2E_{i0}sink_{1}z sin \omega t \ \ \ [V/m] \\ &\vec{H}_{1}(x,t) = Re[\vec{H}_{1}(z)e^{j \omega t}] = \vec{a}_{y}\frac{2E_{i0}}{\eta_{1}}cosk_{1}zcos \omega t \ \ \ [A/m]\end{align}$$These are called **standing waves**, since they do not appear to travel with time. 
![[Pasted image 20221207141925.png|550]]

