---
aliases: [step response, step, stegsvaret]
---
# Stegsvar (aliases: Step response, Step)
An output y from a process when the input *u* (control signal) is given by a step. 
$$\begin{cases} 1, \ \ \ \ \ t \geq 0 \\ 0, \ \ \ \ \ t < 0 \end{cases}$$
![[Pasted image 20220831104437.png|400]]

$$ y(t) = \int_{0}^{t} h(\tau) \, dt$$
The step response is the integral of the impulse response. 

The [[Laplacetransform|laplace transform]] of a step is $1/s$:
$$U(s) = \int_{0}^{\infty} e^{-st} \, dt = \frac{1}{s}$$

Example:
$$Y(s) = \frac{1}{m(s^{2}+g)} \cdot \frac{1}{s}$$
To solve this with laplace transform, [[partialbråksuppdelning]] is recommended.

### See [[Relation between poles and step response]]
#regler 
