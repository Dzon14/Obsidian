---
aliases: [bodediagrammet, bodediagram, bode, bode plot]
tags: [regler]
---
# The Bode plot
Features two curves:
- Magnitude - $\lvert G(i \omega) \rvert$, which is drawn in a logarithmic scale.
- argument/phase - $arg(G(i \omega))$, drawn in a linear scale. 
The frequency axis (x-axis) is logarithmic for both. 
- When having a tough transfer function, it's easier to divide it into "building blocks" and then plotting the bode according to all the separate blocks (then adding the drawings together).

![[Pasted image 20220905112641.png]]

### Example
Bode plot of $$G(s) = (1+sT)^{n}$$
- Magnitude: $$log \lvert G(iw)\rvert = log \lvert 1 + i \omega T \rvert ^{n}= n log \sqrt{1 + \omega ^{2}T^{2}}$$
- Argument: $$narg(1 + i\omega T) = n \cdot arctan(\omega T)$$
- For small values of $\omega$ both the **Magnitude** and the **Argument** will go towards 0. 
- For large values:
$$\begin{cases} log \lvert G(i \omega) \rvert \rightarrow nlog (\omega T) \\ arg(G(i \omega ) \rightarrow n \frac{\pi}{2}\end{cases}$$
- The intersection between the low- and high-frequency asymptotes is given by $$log( \omega T) = 0$$This is the corner frequency (Brytfrekvens) - $\omega = \frac{1}{T}$
![[Pasted image 20220905163902.png|500]]


## From lecture
![[Pasted image 20220905153514.png]]

### Examples 
### Ex 1
$$G(s) = \frac{1}{s+1}$$
![[Pasted image 20220905155722.png]]



 