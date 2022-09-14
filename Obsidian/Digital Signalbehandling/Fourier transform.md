---
aliases: [Fourier, fouriertransform, fouriertransformen]
---
# Fourier transform
lägg in tabell


![[Pasted image 20220912145143.png|650]]


## [[Discrete-time Fourier Transform|DTFT]]
#### For an aperiodic signal
##### Discrete-time
To derive the [[Fourier transform]] we can
1) Create a periodic signal from a finite duration signal $$x_{p}(t) = \sum_{k= - \infty}^{\infty}x(n-kN)$$
2) Represent $x_{p}(t)$ with its fourier coefficients $$c_{k}= \frac{1}{N} \sum_{n=0}^{N-1}x_{p}(n)e^{-j2\pi f_{0}n}$$
3) For large enough $T_{p}$ $$c_{k}= \frac{1}{N} \sum_{-\infty}^{\infty}x(n)e^{-j2\pi f_{0}n}$$
4) (**DTFT**) Define the fourier transform of x(t) as $$X(f) = \sum_{n=-\infty}^{\infty}x(n) e^{-j2\pi fn}$$
- Coefficient: $$c_{k} = \frac{1}{N} \sum_{n=-\infty}^{\infty} x(n)e^{-j2\pi kf_{0}n} = \frac{1}{N}X(kf_{0})$$
#matte 