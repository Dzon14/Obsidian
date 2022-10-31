---
tags: [el]
---
# Continous vs discrete time
- Continous-time signals - the real world, analog circuits etc. 
- Discrete-time signals are typically man made
- Using only discrete-time signals, we can essentially not interact with the real world.
- Discrete-time electronic devices (digital circuits) can be very flexivle and programmable

**How do we get the best of both worlds?**
- An electronic device interacting with the real world, observing an input signal and producing an output signal.
- We mix Continous and Discrete-time signals.
Input -> Sampling (ADC) -> Digital signal processing -> Reconstruction (DAC) -> Output
The **Digital signal processing** step in the middle creates "best of both worlds"

### Continous-time sinusoid ("analog"):
$X_{a(t)}= Acos(\Omega t + \theta) = \frac{A}{2}e^{\Omega t + \theta} + \frac{A}{2}e^{-j(\Omega t + \theta)}$ 
Skrivs om mha Eulers formel. 

### Discrete-time sinusoid
$x(n) = Acos(\omega n + \theta)$, $-\infty < n < \infty$
- Both above can be rewritten in frequency by $w = 2 \pi f$
- A discrete-time sinusiod is only periodic if its frequency is a rational number.
- Discrete-time sinusiods whose angular frequencies are separated by an integer multiple of $2 \pi$ are identical. It's called **aliasing**.
- The highest rate of oscillation in a discrete time sinusiod is attained when $\omega = \pm \pi$
- In Continous omega and frequency is written in big letters and small letters for discrete.
Can also be written as $x(n) = Acos(\omega n + \theta) = \frac{A}{2}e^{j(\omega n + \theta)} + \frac{A}{2}e^{-j(\omega n + \theta)}$

 