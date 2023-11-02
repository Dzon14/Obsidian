---
tags: [el]
aliases: [IIR]
---
# IIR filter
Bibo Stable IIR filters cannot have [[Linear phase]] , if it has a pole outside of the unit circle it's unstable.

- The impulse response is of infinite duration
- The filter is BIBO-stable , if and only if, all its poles are inside the unit circle. 
- The filter cannot have [[Linear phase]]

## Implementation
$$y(n) = - \sum_{k=1}^{N}a_{k}y(n-k) + \sum_{k=0}^{M}b_{k}x(n-k)$$
![[Pasted image 20221005085448.png|500]]
- In practice, numerator and denominator orders, M & N, can often be made "small" (compared to a [[FIR filter]] implementation with similar properties). (+)
- Parametric design, where locations of poles and zeros can help us achieve certain properties (+)
- With poles on the unit circle, we can include resonance phenomena (+)
- Can be unstable (if not designed correctly) (-)
- **Cannot** have [[Linear phase]] (-)