---
tags: [elmagi]
---
# Curl
The curl of a vector field $\vec{A}$ at a point is defined as a vector whose magnitude is the net circulation of $\vec{A}$ (along closed loop C) per unit area as the area (encircled by C) tends to zero, and whose direction is the normal direction of the area when the area is oriented to make the net circulation maximum

## Definition
$$curl \ \vec{A} \overset{\Delta}{=} \lim_{\Delta x\to 0} \frac{1}{\Delta s} \left[\vec{a}_{n} \oint\limits_{C}^{} \vec{A} \cdot \ d \vec{l}  \right]_{max}$$
```math
||{"id":1429034713956}||


```

Also:
$$curl \ \vec{A} = \nabla \times \vec{A}$$

For all the coordinates. See lecture 5 for prove.

## Physical meaning of $\nabla \times \vec{A}$
![[Pasted image 20221003105750.png]]

- For the **point charge**, whose net outward flux for a vanishing close surface around the charge is non-zer0 $\nabla \cdot \vec{A} \neq 0$ . This charge is called a **flow source**
  $\nabla \vec{E} \neq 0$
- For the **long wire** 
  $\nabla \times \vec{B} \neq 0$ 
- Another example is the water flow when emptying a sink

