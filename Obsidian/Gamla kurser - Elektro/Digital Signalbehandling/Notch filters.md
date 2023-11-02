
---
aliases: [IIR filter, FIR filter]
tags: [el]
---
# Notch filters
**Notch filter:**
if your input signal has some disturbance in the form of a (real-valued) sinusoid as a certain frequency $w_{0} = \frac{\pi}{4}$, you may want to design a filter that cancels that particular frequency and lets the rest of the signal through (preferably untouched)

![[Pasted image 20220921092533.png|500]]

We do not get the plot/filter we want, because beside filtering the disturbance it also influences other components. [[Poles]] close to [[Zeros]] can cancel their effect away frrom the location of the zeros, therefore we place the poles just inside the zero (instead of at origin)

We now get:
![[Pasted image 20220921093248.png|500]]

and we get the following plot

![[Pasted image 20220921093334.png|500]]

**Note:** The closer the poles are to the zeros, the more "localized" the effect of the zeros along the frequency axis

## [[FIR filter]]

## [[IIR filter]]

![[Pasted image 20230407180817.png]]