---
tags: [el]
---
# Impulse-invariance transformation
If we have a continous-time (analog) [[Linear and time-invariant (LTI) systems|LTI]] system with [[Impulssvar|impulse response]] $h_{a}(t)$ we can approx it by discrete-time **filtering**, where we use a sampled version of $h_{a}(t)$ as our discrete-time impulse response $$h(n) = h_a (nT)$$
This is called an **impulse-invariance transformation** of our continouse-time system. 

If the analog [[Impulssvar|impulse response]] is NOT bandlimited to half our [[Sampling]] rate , we get [[Aliasing]].

## Example
![[Pasted image 20220926144133.png]]