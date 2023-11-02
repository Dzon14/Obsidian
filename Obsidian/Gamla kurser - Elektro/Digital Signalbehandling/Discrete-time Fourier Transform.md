---
aliases: [DTFT]
---
# DTFT 

#### For an aperiodic signal
##### Discrete-time
To derive the [[Fourier transform]] we can
1) Create a periodic signal from a finite duration signal $$x_{p}(t) = \sum_{k= - \infty}^{\infty}x(n-kN)$$
2) Represent $x_{p}(t)$ with its fourier coefficients $$c_{k}= \frac{1}{N} \sum_{n=0}^{N-1}x_{p}(n)e^{-j2\pi f_{0}n}$$
3) For large enough $T_{p}$ $$c_{k}= \frac{1}{N} \sum_{-\infty}^{\infty}x(n)e^{-j2\pi f_{0}n}$$
4) (**DTFT**) Define the fourier transform of x(t) as $$X(f) = \sum_{n=-\infty}^{\infty}x(n) e^{-j2\pi fn}$$
- Coefficient: $$c_{k} = \frac{1}{N} \sum_{n=-\infty}^{\infty} x(n)e^{-j2\pi kf_{0}n} = \frac{1}{N}X(kf_{0})$$

## [[Relation between z-transform and DTFT]]

## DTFT symmetry properties
Complex signals and transforms composed of real and imaginary parts
$$\begin{align} x(n) = x_{R}(n) + jx_{1}(n) \\ X(\omega) = X_{R}(\omega) + jX_{1}(\omega) \end{align}$$
![[Pasted image 20220914092906.png]] 
![[Pasted image 20220914093142.png]]

## Properties of DTFT
![[Pasted image 20220914093431.png|500]]
$S_{xx}$ is from the energy density spectrum. 

![[Pasted image 20220914093629.png|500]]
**Error:** In frequency shifting, the t in $e^{j \omega_{0} t}$ should be a n.
**Error:** In multiplication, there should be a $\pi$ so we get: $\frac{1}{2\pi}$ 


#el 
