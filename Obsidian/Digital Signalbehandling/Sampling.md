# Sampling
Sampling period T gives a sampling frequency:
$F_{s}= \frac{1}{T}$ , with the unit samples/sec

## Sampling of Analog Signals
There are different ways to sample analog signals. Periodic or Uniform sampling is the most used sampling type. Described by:
$$x(n) = x_a(nT),\ -\infty < n < \infty$$
x(n) is the discrete-time signal, and $x_a$ is the analog signal. 

Periodic sampling gives a relationship between the time variables t and n of continous-time and discrete-time signals. $$t = nT = \frac{n}{F_{s}}$$
![[Pasted image 20220830103913.png|600]]

F (continous) and f (discrete) are related through $$f = \frac{F}{F_{s}}$$
### Ranges
- For continous-time sinusoids: 
	  $-\infty < F < \infty$ , 
	  $-\infty < \Omega < \infty$
- For discrete-time sinusoids:
		$\frac{-1}{2} < f < \frac{1}{2}$, 
		$- \pi < \omega < \pi$

### Relations
![[Pasted image 20220830104536.png]]

#el 