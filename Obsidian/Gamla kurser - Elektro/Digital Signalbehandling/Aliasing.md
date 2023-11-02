---
tags: [el]
aliases: [vikning, aliased, folding]
---
# Aliasing
The original signal contain components outside (its interval?) what will
**leak** into the main interval and distort the shape.
- Adds up contributions of repeated signals

## Anti-aliasing filter on input
![[Pasted image 20220926142545.png]]

## Regler - Vikningseffekten
Samplingsfrekvensen $\omega_{s}= \frac{2 \pi}{h}$
- Vi kan bara "se" frekvensen upp till [[Nyquistfrekvensen]].
- $\omega_{N}= \frac{\omega_{s}}{2}$
- Höga frekvenser tolkas som låga frekvenser - vi måste filtrera! (analoga filter)

1) Sampla tillräckligt ofta.
2) Filtrera bort frekvenser över $\omega_N$. 
