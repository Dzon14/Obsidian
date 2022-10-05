---
tags: [matte]
---
# Line integral 
First off, choose a coordinate system!

![[Pasted image 20220926114527.png|300]]
- The curve C begins from position vector $\vec{R}(u=a)$ and ends at position vector $\vec{R}(u=b)$, with the position vector parameterized by u.
- If $\vec{F}$ is electric force on a charge we get the line integral $$\int_{C}^{} \vec{F} \cdot \ d \vec{l}$$ which is the work done by $\vec{F}$ to move the charge along the curve C.
- By changing the variable we can evaluate the integral in terms of parameter. We can then evaluate the work done as: $$W = - \int_{C}^{} \vec{F} \cdot \ d \vec{l} = - \int_{a}^{b} \vec{F} (\vec{R}(u)) \cdot \ \frac{d \vec{l}}{du} du$$
- **IF** the line integral is **closed**, we call it a circulation of $\vec{F}$ ([[Stoke's theorem]]) $$\text{Circulation of } \vec{F} \text{ along C } = \oint_{C}^{} \vec{F} \cdot \ d \vec{l}$$
- Remember that $d \vec{l}$ is depending on what coordinate system your're using,
  for instance, [[Cartesian Coordinates]] have $$d \vec{l} = \vec{a}_{x}dx + \vec{a}_{y}dy + \vec{a}_{z}dz$$
  

