---
tags: [komsys]
---
# Data and Signals


## Data vs Signal
- Data: Static representation of information 
		- For storage
-  Signals: Dynamic representation of information
		- For transmission
![[Pasted image 20230117154306.png|400]]

## Digitalization of analog signals
Three steps:
1. [[Sampling]]
   - Discretization in time
2. [[quantization]]
   - Discretizatioin in amplitude
3. Encoding
   - Binary representation of amplitude levels

- ADC or DAC.

## [[Sampling]]

- The process of discretizing time of a continous signal $$s(n) = s(nT_{s})$$
- Sample time: $T_{s}$
- Sample frequency: $F_{S} = \frac{1}{T_{S}}$
- Must save information about sampling time

## [[Nyquist sampling theorem]]

## [[Aliasing]]

## [[quantization]]
- Uniform quantization for k bits
- $M=2^{k}$ equidistant levels
- Represent sample with k bits
![[Pasted image 20230117162035.png|300]]

## Encoding
- Representation of quantized samples in bits ![[Pasted image 20230117162115.png|400]]
- Detta föra tt kunna lagra signalen i binär form.

## Example: Data rate for telephony
![[Pasted image 20230117163109.png|500]]
