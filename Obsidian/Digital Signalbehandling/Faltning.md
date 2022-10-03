---
aliases: [convolution, faltas, linear convolution]
tags: [el]
---
# Faltning 
(Convolution)
**Continous:**
$$x_{1}(t) \ast x_{2}(t) = \int_{}^{} x_{1}\tau x_{2}(t- \tau) \, dt$$

**Discrete:**
$$x_{1}(n) \ast x_{2}(n) = \sum_{k}^{} x_{1}(k) x_{2}(n-k)$$

Using a table to calculate the convolution:
- Use one signal for the columns and one for the rows.
- Calculate all products of individual values
- Sum along diagonals
![[Pasted image 20220831085016.png|400]]

### Properties of convolution
- Unit impulse is the identity element of convolution. ![[Pasted image 20220831085655.png]]
- It fulfills the commutative law.
- the associative law
- the distributive law

### BIBO stability of LTI Systems
- A system is BIBO stable if and only if a bounded input produces a bounded output
An LTI system (from previous):
$$y(n) = \sum_{k = -\infty}^{\infty}x(k)h(n-k)$$
- A bounded input x(n) implies that $\lvert x(n) \rvert \leq M_{x}$, for some finite positive number $M_{x}$ and we get ![[Pasted image 20220831084512.png]]
**Conclusion:** An LTI system is BIBO stable if it's impulse response h(n) is absolutely summable. (Important)

## Using the [[Discrete Fourier transform|DFT]] for linear convolution
1) Zero-pad both sequences, of length K and L, to a common length $N \geq K+L-1$
2) Calculate the N-point [[Discrete Fourier transform|DFT]] of both sequences.
3) Multiply the two DFTs
4) Perform an N-point inverse DFT (IDFT) on the product
