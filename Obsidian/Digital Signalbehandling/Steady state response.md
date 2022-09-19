## Steady state response 
What happens if the sinusoidal starts as some time $n_{0}$?
We get two components, the [[transient]] and the steady-state component.

- All BIBO stable LTI systems have this behaviour (in general).
- If the system is BIBO stable ($\lvert a \rvert < 1$) all terms including $a^{n+1}$ will disappear with time and are called [[transient]], while what remains is the **steady state**.

### Response to periodic signals
Input signal $x(n)$ is periodic with fundamental peron $N$, it can be written as a [[Fourierserie|fourier series]] $$x(n) = \sum_{n=0}^{N-1}c_{k}e^{j2 \pi kn/N}$$
With the linearity property we get $$y(n) = \sum_{n=0}^{N-1}c_{k}H \left(\frac{2\pi}{N}k \right)e^{j2\pi kn/N}$$
We conclude that the output is also a periodic signal, with the same period N. 
- In short, an LTI system can change the shape of a periodic signal, but **not** its period.

### Response to aperiodic signals
**Reminder:** $y(n) = h(n) * x(n)$ which gives us (convolution property) $Y(\omega) = H(\omega)X(\omega)$, which also can be written in polar form ..

- The magnitude and phase of $H(\omega)$ shows how the LTI system influences mag and phase of the input signal $X(\omega)$ at different frequencies $\omega$.

#el 