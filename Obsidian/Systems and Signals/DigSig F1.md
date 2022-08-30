
# Digital Signalbehandling F1

## Continous vs discrete time
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
$x(n) = Acos(\omega n + \theta)$
- Both above can be rewritten in frequency by $w = 2 \pi f$
- A discrete-time sinusiod is only periodic if its frequency is a rational number.
- Discrete-time sinusiods whose angular frequencies are separated by an integer multiple of $2 \pi$ are identical. It's called **aliasing**.
- The highest rate of oscillation in a discrete time sinusiod is attained when $\omega = \pm \pi$
- In Continous omega and frequency is written in big letters and small letters for discrete.

## Sampling and reconstruction
Sampling period T gives a sampling frequency:
$F_{s}= \frac{1}{T}$ , with the unit samples/sec

## Kronecker delta function
$$\delta (n) = \begin{cases} 1 \ \text{if n = 0} \\ 0 \ \text{otherwise} \end{cases}$$
## Unit step function
$$u(n) = \begin{cases} 1 \ \text{if } n\geq 0 \\ 0 \ \text{otherwise} \end{cases} $$

## Discrete-time signals
- It can be written as a sum of impulse
- The exponential signal is a sequence on the form $x(n) = a^{n}$ 
  and if a is complex, $a = re^{j \theta}$, then (polar form)
  $x(n) = r^{n}e^{j \theta n}$

## Signal symmetries
- A signal x(n) is said to be symmetric or even if $x(n) = x(-n)$
  and antisymmetric or odd if $x(n) = -x(-n)$
- Any signal x(n) can be written as a sum of an even and an odd signal $$x(n) = x_{e(n)}+ x_o(n)$$