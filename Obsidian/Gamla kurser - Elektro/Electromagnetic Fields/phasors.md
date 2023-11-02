---
tags: [el]
---
# Phasors
(Use of Phasors for Time-Harmonic Fields)

In electrical engineering, we often deal with periodic signals expressed as sinusoidal (sine, cosine) functions. Since [[Maxwell's equations]] are linear differential equations, sinusoidal source functions of a given frequency will also result in $\vec{E}$ and $\vec{H}$ fields with the same frequency at steady state.

Moreover, any periodic signals in the time domain can be decomposed into sine/cosine components via [[Fourierserie|fourier series]] expansion. This means we can solve the problem of arbitrary periodic signals in general by solving for the sinusoidal components and then combining the solutions with superposition to get the total field

- Linear diff. equations - does not change the frequency of the source.

$$\begin{align} &e^{jx} = cosx + jsin x \\ &i(t) = Icos(\omega t + \phi) \\ &i(t) = Re \left( Ie^{j(\omega t + \phi)} \right) = Re \left( I_{s}e^{j \omega t} \right) \end{align}$$
where $I_{s} = Ie^{j \phi}$ is the **phasor** form for $i(t)$.
We have used $cos \omega t$ as the reference phase. 

## Example
![[Pasted image 20221130115556.png]]