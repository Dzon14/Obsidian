---
aliases: [impulse response, impulse, impuls, impulssvaret]
---
# Impulssvar
![[Pasted image 20220831104446.png|400]]
$$y(t) = \int_{0}^{t} h(t - \tau)u(\tau) \, d \tau$$
The [[Laplacetransform|laplace transform]] of an impulse is 1:
$$U(s) = \int_{0}^{\infty} e^{st} \delta \, dt = 1$$
Hence, the laplace transformation is given by the transfer function $$G(s) = \frac{Y(s)}{U(s)} = Y(s)$$
Example:
$$Y(s) = \frac{1}{m(s^{2}+g)} \cdot 1 = (Laplace) = \frac{1}{m} \cdot \left(\frac{1}{\sqrt{g}} \cdot \frac{\sqrt{g}}{s^{2}+g}\right)= \frac{1}{m \sqrt{g}} sin(\sqrt{g} \cdot t)$$ 
# DigSig

## Impulse response of an ideal LP filter
cut-off freq $w_{c}$
![[Pasted image 20220919143452.png]]
For the ideal low-pass (LP) [[filter]], only the magnitude of the signal is affected, **not** the phase. The frequency response should be $$H(\omega) = \begin{cases} 1 \ \ \text{if} \ \ -\omega_{c}< \omega< \omega_{c} \\  0 \ \ \text{elsewhere} \end{cases}$$
By applying the inverse [[Discrete-time Fourier Transform|DTFT]] formula, we get $$h(n) = ... = \frac{sin(\pi \omega_{c}n)}{\pi n} = \omega_{c}sinc(\omega_{c} n)$$
which is a sinc function. We can't build this filter since it's infinitely long.
It is a nice filter in the frequency domain, but not realistic.

#regler