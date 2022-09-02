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
#regler