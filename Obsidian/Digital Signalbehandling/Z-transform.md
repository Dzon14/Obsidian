---
aliases: [Z-transformen, Z-transformer]
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

#el