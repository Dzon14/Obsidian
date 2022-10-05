---
tags: [el]
aliases: [FIR]
---
# FIR filter
![[Pasted image 20220921095412.png|500]]
[[Linear phase]] requires each zero inside the unit circle has a corresponding one outside the unit circle
- The impulse response is of finite duration
- The filter is always BIBO stable
- All poles are at the origin (z=0)
- The filter may have [[Linear phase]]
- The filter is minimum-phase if all its zeros are inside the unit circle.

## Implementation
$$y(n) = \sum_{k=0}^{M-1}h(k)x(n-k)$$
![[Pasted image 20221005084726.png]]
+ Always stable (M limited) (+)
+ Can be made with [[Linear phase]] - if [[Impulssvar|impulse response]] symmetric (+)
+ In practice, the [[Impulssvar|impulse response]] often needs to be long to fulfill requirements. (-)
+ Difficult to include resonance phenomena (since they, by nature, are stable) (-)