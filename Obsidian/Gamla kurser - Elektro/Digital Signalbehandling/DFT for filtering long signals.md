---
tags: [el]
---
# [[Discrete Fourier transform|DFT]] for filtering long signals 
One method for splitting the long convolution into shorter oness is the **overlap-add method**

Assume we have a system with [[Impulssvar|impulse response]] h(n), of duration K, and much longer input x(n), where the output signal is calculated using [[Faltning|linear convolution]] $$y(n) = h(n) * x(n)$$
By splitting it into **non-overlapping blocks** $x_{m}(n)$, each of length L $$x_{m}(n) = \begin{cases} x_{m}(n) \ \ \text{ for } mL \leq n < (m+1)L \\ 0 \ \ \text{ otherwise }\end{cases}$$
we can write the input signal $$x(n) = \sum_{M= - \infty}^{\infty}x_{m}(n)$$
and (linearity property) $$y(n) = h(n) * x(n) = h(n) * \left( \sum_{m= -\infty}^{\infty}x_{m}(n) 
 \right) = \sum_{m= - \infty}^{\infty}y_{m}(n)$$
 where $y_{m}(n) = h(n) * x_{m}(n)$.

We have now made a series of shorter convolutions, who (added together) give the same output.

## Ilustration
![[Pasted image 20221003135306.png]]
- where 
1) Zero-pad $h(n)$ to length $N$
2) Calculate $H(k) = DFT(h(n))$
3) For each input block $x_{m}(n)$
	- Zero-pad $x_{m}(n)$ to length N
	- Calculate $X_{m}(k) = DFT(x_{m}(n))$
	- Calculate $Y_{m}(k) = H(k)X_{m}(k)$
	- Calculate $y_{m}(n) = IDFT (Y_{m}(k))$
	- Add $y_{n}$ to previous output (at correct position/correct overlap)