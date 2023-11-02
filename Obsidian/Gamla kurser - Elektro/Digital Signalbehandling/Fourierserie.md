---
aliases: [fourier series]
---
# Fourierserie

## Fourier series of periodic signals

##### Continous-time:
- Has the property $x(t) = x(t + T_{p})$
- A fundamental frequency $F_{0} = 1/T_{p}$

Fourier series is written as $$x(t) = \sum_{k=-\infty}^{\infty}c_{k}e^{j2\pi kF_{0}t}$$
where the Fourier coefficients are $$c_{k}= \frac{1}{T_{p}}\int_{T_{p}}^{}  x(t)e^{-j2\pi kF_{0}t} \ dt$$
##### Discrete-time
- has the property $$x(n)= x(n+N)$$
- A fundamental frequency $f_{0}= \frac{1}{N})$

Fourier series is written as $$x(n) = \sum_{k=0}^{N-1}c_{k}e^{j2\pi kf_{0}n}$$
where the Fourier coefficients are $$c_{k}= \frac{1}{N} \sum_{n= 0}^{N-1} x(n)e^{-j2\pi kf_{0}n}$$
- The coefficients are called the **spectrum** of the signal.

## Fourier series of aperiodic signals
### Continous-time
To derive the [[Fourier transform]] we can
1) Create a periodic signal from a finite duration signal $$x_{p}(t) = \sum_{k= - \infty}^{\infty}x(t-kT_{p})$$
2) Represent $x_{p}(t)$ with its fourier coefficients $$c_{k}= \frac{1}{T_{p}}\int_{\frac{-T_{p}}{2}}^{\frac{T_p}{2}} x_{p}(t)e^{-j2\pi kF_{0}t} \, dt$$
3) For lare enoug $T_{p}$ $$c_{k}= \frac{1}{T_{p}}\int_{-\infty}^{\infty} x(t)e^{-j2\pi}k F_{0}t \, dt$$
4) Define the fourier transform of x(t) as $$X(F) = \int_{-\infty}^{\infty}x(t)e^{-j2\pi Ft}  \, dt$$
- The coefficient can be written as $$c_{k}= \frac{1}{T_{p}} \int_{-\infty}^{\infty} x(t) e^{-j2\pi kF_{0}t} \ dt = \frac{1}{T_{p}}X(kF_0)$$
### Discrete-time
To derive the [[Fourier transform]] we can
1) Create a periodic signal from a finite duration signal $$x_{p}(t) = \sum_{k= - \infty}^{\infty}x(n-kN)$$
2) Represent $x_{p}(t)$ with its fourier coefficients $$c_{k}= \frac{1}{N} \sum_{n=0}^{N-1}x_{p}(n)e^{-j2\pi f_{0}n}$$
3) For large enough $T_{p}$ $$c_{k}= \frac{1}{N} \sum_{-\infty}^{\infty}x(n)e^{-j2\pi f_{0}n}$$
4) (**[[Discrete-time Fourier Transform|DTFT]]**) Define the fourier transform of x(t) as $$X(f) = \sum_{n=-\infty}^{\infty}x(n) e^{-j2\pi fn}$$
- Coefficient: $$c_{k} = \frac{1}{N} \sum_{n=-\infty}^{\infty} x(n)e^{-j2\pi kf_{0}n} = \frac{1}{N}X(kf_{0})$$
## Behavior
![[Pasted image 20220912145343.png|600]]


#matte 

 
