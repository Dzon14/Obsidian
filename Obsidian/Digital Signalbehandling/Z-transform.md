---
aliases: [Z-transformen, Z-transformer]
tags: [el]
---

# Z-transform
- Plays the same role in the analysis of discrete-time signals as the [[Laplacetransform|laplace transform]] does for continous-time signals (and LTI systems). 
- By using the table of properties and pairs, Z-transform problems can be solved in the same way as [[Fourier transform]] / laplace. 
### Direct z-transform
- Called direct because it transforms the time-domain signal $x(n)$ into its complex-plane representation $X(z)$.

**Definition:**
$$X(z) = \sum_{n = - \infty}^{\infty} x(n)z^{-n}$$
- can be seen "as simple as" writing our sequence/signals as a polynomial/power series in z. The exponent on z shows the position of each value in time. (delay, compared to n = 0).
- Relationship between $x(n)$ and $X(z)$ is indicated by $$x(n) \overset{z}{\longleftrightarrow} X(z)$$
$$$$
### Inverse Z-transform
$$x(n) = \frac{1}{2\pi j} \oint_{C}^{} X(z) z^{n-1} \, dz$$
where $C$ is a closed contour (curve) in the [[Region of convergence]] of $X(z)$.

### The typical procedure 
![[Pasted image 20220905145228.png|300]]

### Properties of the z-transform
![[Pasted image 20220905135943.png|730]]
![[Pasted image 20220905140028.png|650]]

### Common z-transform pairs 
![[Pasted image 20220905142227.png|500]]


## [[Poles]] and [[Zeros]] of z-transforms
Rational functions are important in z-transforms: $$X(z)=\frac{B(z)}{A(z)}$$
By simplifying and factorising in multiple steps we get a factored equation using their roots. 
![[Pasted image 20220907085330.png|500]]
- The finite numerator roots are called **zeros**.
- The finite denominator roots are called **poles**.

$$\begin{align} X(z_k)= 0\ \ \ \text{if $z_k$ is a zero} \\ X(p_k) = \infty \ \ \ \text{if $p_{k}$ is a pole} \end{align}$$
Meaning that the [[Region of convergence|ROC]] **cannot** contain any poles

They can have different orders. 
If M ≠ N the $z^{-M+N}$ term also contributes with |M - N| zeros or poles at the origin z = 0, depending on the sign of -M + N

- The location of poles and zeros in the C-plane reveals the general behaviour of a system and the signal/sequence.

![[Pasted image 20220907085657.png|400]]

If we have a signal $$a^{n}u(n) \longleftrightarrow \frac{1}{a-az^{-1}}$$
we get the following signle real pole location (Ex. a = 0, a = 1, a = 2):
![[Pasted image 20220907092239.png|600]]

**Important:**
$$\text{Poles and Zeros are conjugate pairs} \longleftrightarrow \text{real signal in time}$$
- We say that a causal signal is [[Stabilitet|stable]] if all its poles are inside the unit circle.
See [[Kausalitet|causality]]

### Causal LTI system BIBO stability
- The location of poles of the **system** function characterizes BIBO stability.
- For a casual and BIBO stable system with impulse response $h(n)$ 
	A. Causality implies that the impulse response must fulfill $$h(n) = \text{for } n<0$$
	B. BIBO stability requires that $$\sum_{n=\infty}^{\infty} \lvert h(n) \rvert < \infty$$
	A and B say that the radius r, outside which we have the [[Region of convergence|ROC]] ,must be r<1.

![[Pasted image 20220907094737.png||450]]

### Non-relaxed systems and the $Z^{+}$-transform
(also one-sided z-transform)
Relaxed - zero content in ther delay units.

**Definition**
$$Y^{+}(z) = \sum_{n= 0}^{\infty} y(n)z^{-n}$$
- For [[Kausalitet|casual]] signals, this transform deliver the same result as the normal z-transform. 
- We get a different time-shift property (delay by k)
$$y(n-k) \overset{z^{+}}{\longleftrightarrow} z^{-k}(Y^{+}(z) + \sum_{n=1}^{k}y(-n)z^{n})$$
(skriv stor parantes)
- $Y^{+}(z)$ gives a contribution from $y(n)$ for positive $n \geq 0$ 
- The sum gives new values of $y(n)$ from $n < 0$

## Bevis 
[Z-transform - Wikipedia](https://en.wikipedia.org/wiki/Z-transform)
