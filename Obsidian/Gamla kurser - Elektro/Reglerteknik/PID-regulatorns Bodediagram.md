---
tags: [regler]
aliases: [bode plot of the PID controller]
---
# PID-regulatorns Bodediagram
Man kan använda det öppna systemets Bodediagram för att bestämma [[Kompensering]]slänkar som ger slutna systemet önskade egenskaper. Samma metodik används vid undersökning av PID-regulatorns funktion och parametrarnas betydelse

$$G_{R}' = K' \left( 1+ \frac{1}{sT_{i}'} \right)(1+sT_{d}') = \frac{K' (1+sT_{i}')(1+sT_{d}')}{sT_{i}'}$$
Finns två brytpunkter i nedan diagram, första vid $\omega = \frac{1}{T_{i}'}$ och den andra vid $\omega = 1/T_{d}'$ 
Båda punkter är nollställen och kommer bryta upp diagrammet. 
![[Pasted image 20220927160146.png]]

## [[PID-regulatorns parametrar]]
