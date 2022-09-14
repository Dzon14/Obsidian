---
aliases: [pole, poler, polerna, polen]
---

# Poles

see [[Z-transform]]

## Poles on the unit circle
if $X(z)$ we have poles on the unit circle, the unit circle is not included in the [[Region of convergence|ROC]], and the [[Discrete-time Fourier Transform|DTFT]] does not exist.

There are some important z-transform where this happens:
- The unit step
- The sinusiodal signal
- The Dirac impulse ($\delta (\omega)$)
		- Important consequence (reminder) $$\int_{-\infty}^{\infty} g(\omega)\delta(\omega - \omega_0) \ d \omega = g(\omega_0)$$
Important unstable signals (who have poles on the unit circle)
- Cosine
- Sine
- Unit step
These are only valid inside $-\pi < \omega < \pi$ 

#el 